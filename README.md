**Overview**

This project involves the development and deployment of a logistic regression model to predict whether customers will pay their invoices on time. The model uses historical data on customer transactions to forecast payment behavior, helping businesses manage cash flow, optimize credit terms, and enhance collection strategies.

**Dataset**

The dataset contains 3702 entries with the following columns:

Customer_ID: Unique identifier for the customer
Document Number: Invoice number
Document Date: Date when the document was issued
Net due date: Due date for the payment
Amount in doc. curr.: Amount in the document currency
Document type: Type of document (e.g., invoice, credit memo)
Local Currency: Currency used locally
Posting Date: Date when the document was posted
Payment date: Date when the payment was made
Invoice reference: Reference to the original invoice
Document currency: Currency used in the document
Eff.exchange rate: Effective exchange rate
Clearing Document: Reference to the clearing document
Name 1: Name of the customer

**Model Features**

**The following features were engineered for the model:**

Days_to_due: Number of days from the document date to the due date
Days_to_payment: Number of days from the document date to the payment date
Paid_on_time: Boolean indicating whether the payment was made on time

**Model Training
Data Preprocessing**

Convert date columns (Document Date, Net due date, Posting Date, Payment date) to datetime objects.
Convert numerical columns (Amount in doc. curr., Eff.exchange rate) to float.
Encode categorical variables (Document type, Local Currency, Document currency, Name 1) using Label Encoding.

**Feature Selection**

Customer_ID
Amount in doc. curr.
Document type
Local Currency
Posting Date
Days_to_due
Target Variable:

**Paid_on_time
Train-Test Split**

Split the data into training (80%) and testing (20%) sets.

**Standardization**

Standardize the feature values using StandardScaler.

**Model Training**

Train a LogisticRegression model on the training set.

**Evaluation
The model was evaluated using the following metrics**

Accuracy: 1.00
Precision: 1.00
Recall: 0.99
F1 Score: 1.00

**Confusion Matrix**

[[523   0]
 [  2 216]]
 
**Classification Report**

              precision    recall  f1-score   support

           0       1.00      1.00      1.00       523
           1       1.00      0.99      1.00       218

    accuracy                           1.00       741
   macro avg       1.00      1.00      1.00       741
weighted avg       1.00      1.00      1.00       741

**How to Use
Installation**

Ensure you have Python installed.
Install the required libraries using:

pip install pandas numpy scikit-learn
Code Execution:

Load the dataset.
Preprocess the data as described.
Train the logistic regression model.
Evaluate the model using the provided metrics.
Conclusion
This logistic regression model provides an effective way to predict customer payment behavior. With high accuracy and precision, it can be a valuable tool for businesses to manage cash flow and optimize their collection strategies.
