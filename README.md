# Credit Card Fraud Detection
This repository contains the implementation of a credit card fraud detection model using machine learning techniques. The goal of this project is to identify fraudulent transactions in a highly imbalanced dataset.

## Project Overview
Credit card fraud detection is a critical task for financial institutions to prevent unauthorized transactions and protect users. This project utilizes data preprocessing, resampling techniques, and machine learning algorithms to build a robust fraud detection model.

## Dataset
The dataset used in this project contains transactions made by credit cards, labeled as fraudulent or non-fraudulent. The dataset is highly imbalanced, with a minority of transactions being fraudulent.

## Features
LIMIT_BAL: This feature represents the credit limit assigned to the individual's credit card. It indicates the maximum amount of credit the person can utilize.

SEX: This feature represents the gender of the credit card holder. While gender itself may not directly impact credit card fault detection, it can be considered as a demographic factor that might have some influence on creditworthiness.

EDUCATION: This feature indicates the educational background of the credit card holder. It can provide insights into the person's level of education, which might indirectly correlate with their financial stability and ability to manage credit.

MARRIAGE: This feature represents the marital status of the credit card holder. Similar to gender, marital status can be a demographic factor that could potentially impact credit card fault detection.

AGE: This feature denotes the age of the credit card holder. Age can be an important factor in assessing creditworthiness as it often correlates with financial responsibility and stability.

PAY_0, PAY_2, PAY_3, PAY_4, PAY_5, PAY_6: These features represent the repayment status of the credit card for the past six months. The values indicate the payment status (e.g., -1 represents payment delay for one month, 0 represents payment on time, 1 represents payment delay for two months, and so on). These features are crucial in determining the payment behavior of the individual over time.

BILL_AMT1, BILL_AMT2, BILL_AMT3, BILL_AMT4, BILL_AMT5, BILL_AMT6: These features represent the amount of bill statement for the respective months. They provide information about the outstanding balance on the credit card at specific points in time.

PAY_AMT1, PAY_AMT2, PAY_AMT3, PAY_AMT4, PAY_AMT5, PAY_AMT6: These features represent the amount of payment made by the credit card holder for the respective months. They indicate the actual payments made to reduce the outstanding balance.

default payment next month: This is the target variable or the dependent variable that indicates whether the credit card holder defaulted on their payment in the following month (1 for default, 0 for no default). This is the variable that the credit card fault detection model aims to predict.

## Usage
Data Preprocessing:Load the dataset.
Normalize/standardize features if necessary.
Split the data into training and testing sets.

Resampling:Apply SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance.

Model Training:Train a Random Forest classifier and a Gaussian Naive Bayes model.
Perform hyperparameter tuning to optimize the models.

Evaluation:Evaluate the models using metrics such as accuracy, precision, recall, and F1 score.
Compare the performance of different models and choose the best one.

## Results
After applying SMOTE and hyperparameter tuning, the Random Forest model achieved an overall accuracy of 80.7% and balanced F1 scores of 81% for both classes. In contrast, the Gaussian Naive Bayes model had an overall accuracy of 55% with F1 scores of 29% for non-fraudulent transactions and 67% for fraudulent transactions. Thus, the Random Forest model was selected as the best model for this task.
