


MASTER OF SCIENCE IN INFORMATION TECHNOLOGY


MSIT 723 - ARTIFICIAL INTELLIGENCE AND EXPERT SYSTEMS

PROJECT

MEMBERS

CLIFFORD O.OBIEWA

AUGUSTINE KIBET

IAN KIPROTICH

CREDIT SCORING MODEL 

Link  to the Document 🔗 : https://docs.google.com/document/d/1DypZrtZ-Xm_MAZoDNVIiZo9D9d5W9xhS1SIVeCztU94/edit?usp=sharing
PROBLEM DEFINITION & OBJECTIVE
Over the years a local commercial bank has collected basic bank details and gathered a lot of credit-related information. The management wants to build an intelligent system to segregate the people into credit score brackets to reduce the manual efforts.
The main objective is to build a machine learning model that can classify the credit score.
Objectives of a Credit Scoring Model
1. Assess the Creditworthiness of Borrowers
To evaluate the likelihood that an applicant will repay a loan based on historical and current financial information.
2. Quantify the Probability of Default (PD)
To estimate the statistical probability that a borrower may fail to meet their debt obligations.
3. Support Risk-Based Lending Decisions
To provide financial institutions with an objective basis for loan approval, rejection, or pricing based on risk exposure.
4. Standardize Credit Evaluation
To replace subjective manual assessments with consistent, data-driven credit risk evaluation across all customers.
DATA ACQUISITION
This data has been sourced from Kaggle and has a total of 28 features.
The table below shows the dataset.


Name of feature
Description of feature
ID
Represents a unique identification of an entry
Customer_ID
Represents a unique identification of a person
Month
Represents the month of the year
Name
Represents the name of a person
Age
Represents the age of a person
SSN
Represents the social security number of a person
Occupation
Represents the occupation of a person
Annual_Income
Represents the annual income of the person
Monthly_Inhand_Salary
Represents the monthly base salary of a person
Num_Bank_Accounts
Represents the number of bank accounts a person holds
Num_Credit_Card
Represents the number of other credit cards held by a person
Interest_Rate
Represents the interest rate on a credit card
Num_of_Loan
Represents the number of loans taken from the bank
Type_of_Loan
Represents the types of loan taken by a person
Delay_from_due_date
Represents the average number of days delayed from the payment date
Num_of_Delayed_Payment
Represents the average number of payments delayed by a person
Changed_Credit_Limit
Represents the percentage change in credit card limit
Num_Credit_Inquiries
Represents the number of credit card inquiries
Credit_Mix
Represents the classification of the mix of credits
Outstanding_Debt
Represents the remaining debt to be paid
Credit_Utilization_Ratio
Represents the utilization ratio of credit card
Credit_History_Age
Represents the age of credit history of the person
Payment_of_Min_Amount
Represents whether only the minimum amount was paid by the person
Total_EMI_per_month
Represents the monthly EMI payments
Amount_invested_monthly
Represents the monthly amount invested by the customer
Payment_Behavior
Represents the payment behavior of the customer
Monthly_Balance
Represents the monthly balance amount of the customer
Credit_Score
Represents the bracket of credit score



DATA CLEANING & PREPROCESSING
i) Handling missing values
Checking for missing values (Code)

Checking for missing values (Results)

The following columns have missing values: Name, Monthly_Inhand_Salary, Type_of_Loan, Num_of_Delayed_Payment, Num_Credit_Inquiries, Credit_History_Age, Amount_invested_monthly, Monthly_Balance
Handling missing values using median and mode (Code)
               
Handled missing values using median and mode (Results)

ii) Handling duplicates
Code

Results

iii) Handling outliers
Code

Results

In summary, the following transformations have been made to the data set: 
iv) Split dataset into training and test sets
Code

Step
Action
Purpose
1. Load data
Reads the CSV into a DataFrame.
Base for cleaning operations.
2. Handle missing values
Fills numeric with median and categorical with mode.
Keeps the dataset consistent.
3. Handle duplicates
Drops identical rows.
Removes redundancy.
4. Handle outliers (IQR method)
Removes extreme numeric values outside 1.5×IQR.
Reduces skewness.
5. Save cleaned data
Outputs cleaned dataset.
Ready for analysis or ML.



EXPLORATORY DATA ANALYSIS (EDA)
Histograms



Identify correlations
i) Code

ii) Output: There is no variable that is closely correlated

Featuring Engineering 
Remove irrelevant or redundant features
i) Automatically remove columns with too many missing values

ii) Remove columns with low variance
This is removed as they do not add useful information
Code

Output

F
F
F
F
F
f
F
F
F
F
F
F
F
F
F
F



