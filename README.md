# Current_Project
Loan Approval Prediction using Machine Learning
An end-to-end Python-based data science project that predicts whether a loan application will be approved based on applicant information. The project demonstrates a complete machine learning pipeline — from data exploration to model evaluation.

📌 Project Overview
The objective of this project is to automate the loan eligibility process for financial institutions. By analyzing applicant details such as income, credit history, loan amount, and demographic information, the model predicts whether a loan should be approved (Y) or rejected (N).
This helps banks reduce manual effort, minimize human bias, and improve decision-making speed.
🛠️ Data Preprocessing & Feature Engineering
1. Handling Missing Values

Categorical columns (Gender, Married, Dependents, Self_Employed, Credit_History): Imputed using Mode
LoanAmount: Imputed using Mean
Loan_Amount_Term: Imputed using Median

2. Feature Encoding

Binary categorical variables (Gender, Married, Self_Employed, Education, Loan_Status) → Label Encoding (0/1)
Multi-class variables (Property_Area, Dependents) → One-Hot Encoding

3. Feature Creation

Total_Income = ApplicantIncome + CoapplicantIncome
Income_Loan_Ratio = Total_Income / LoanAmount
LoanAmount_log = Log transformation of LoanAmount (to reduce skewness)

4. Feature Scaling

Applied StandardScaler on all numerical features for distance-based algorithms.
Loan Approval Prediction using Machine Learning
This repository contains a complete end-to-end Python-based data science project that predicts loan approval status. It includes exploratory data analysis, data cleaning, feature engineering, and a comparative evaluation of multiple classification models.
📌 Project Overview
The goal of this project is to automate the loan eligibility process based on applicant details provided while filling out online application forms. These details include Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History, and others.
📊 Dataset Description
The dataset consists of 614 observations and 13 features before preprocessing:
Feature NameDescriptionGenderMale/FemaleMarriedApplicant married (Yes/No)DependentsNumber of dependents (0, 1, 2, 3+)EducationApplicant Education (Graduate/Undergraduate)Self_EmployedSelf-employed (Yes/No)ApplicantIncomeApplicant incomeCoapplicantIncomeCo-applicant incomeLoanAmountLoan amount in thousandsLoan_Amount_TermTerm of loan in monthsCredit_HistoryCredit history meets guidelines (1.0/0.0)Property_AreaUrban/Semiurban/RuralLoan_StatusLoan approved (Y/N) [Target Variable]
🛠️ Data Preprocessing & Feature Engineering
To prepare the data for training, several cleaning and engineering steps were taken:

Handling Missing Values:

  * Categorical features (Gender, Married, Dependents, Self_Employed, Credit_History) were imputed using their mode.
  * LoanAmount was imputed using the mean.
  * Loan_Amount_Term was imputed using the median.

Feature Transformation & Encoding:

  * Categorical variables like Gender, Married, Self_Employed, Education, and Loan_Status were mapped to numeric binary values.
  * Multi-class variables (Property_Area, Dependents) were converted into numeric features using One-Hot Encoding (pd.get_dummies).

New Features Created:

  * Income_Loan_Ratio: Total income (Applicant + Coapplicant) divided by the loan amount.
  * LoanAmount_log: Log transformation applied to the LoanAmount to reduce skewness.

Feature Scaling: All features were scaled using StandardScaler to normalize the data before training distance-based models.

🤖 Models Evaluated & Performance
Four different classification models were trained and evaluated using 5-fold cross-validation:
ModelCross-Validation AccuracyLogistic Regression80.782%Decision Tree79.144%Random Forest77.853%K-Nearest Neighbors75.566%
 
 
#make it more structure✅ Improved & Well-Structured Version

Loan Approval Prediction using Machine Learning
An end-to-end Python-based data science project that predicts whether a loan application will be approved based on applicant information. The project demonstrates a complete machine learning pipeline — from data exploration to model evaluation.
  

📌 Project Overview
The objective of this project is to automate the loan eligibility process for financial institutions. By analyzing applicant details such as income, credit history, loan amount, and demographic information, the model predicts whether a loan should be approved (Y) or rejected (N).
This helps banks reduce manual effort, minimize human bias, and improve decision-making speed.

🛠️ Data Preprocessing & Feature Engineering
1. Handling Missing Values

Categorical columns (Gender, Married, Dependents, Self_Employed, Credit_History): Imputed using Mode
LoanAmount: Imputed using Mean
Loan_Amount_Term: Imputed using Median

2. Feature Encoding

Binary categorical variables (Gender, Married, Self_Employed, Education, Loan_Status) → Label Encoding (0/1)
Multi-class variables (Property_Area, Dependents) → One-Hot Encoding

3. Feature Creation

Total_Income = ApplicantIncome + CoapplicantIncome
Income_Loan_Ratio = Total_Income / LoanAmount
LoanAmount_log = Log transformation of LoanAmount (to reduce skewness)

4. Feature Scaling

Applied StandardScaler on all numerical features for distance-based algorithms.


🤖 Models Evaluated
Multiple classification algorithms were trained and compared using 5-Fold Cross-Validation.
Model,Cross-Validation Accuracy,Rank
Logistic Regression,80.78%,1
Decision Tree,79.14%,2
Random Forest,77.85%,3
K-Nearest Neighbors,75.57%,4

Loan-Approval-Prediction/
├── data/
│   └── loan_data.csv
├── notebooks/
│   └── EDA_and_Modeling.ipynb
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   └── model_training.py
├── models/
├── results/
├── requirements.txt
├── README.md
└── main.py
