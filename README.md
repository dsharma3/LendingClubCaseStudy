
# Lending Company Case Study

This project involves a detailed analysis of loan data to uncover insights and patterns that can be useful for financial decision-making. The notebook processes, analyzes, and visualizes loan data to identify key factors influencing loan status.

## Table of Contents
1. [Introduction](#Introduction)
2. [Data Description](#data-description)
3. [Data Cleaning, Filtering and Imputing](#data-cleaning-filtering-and-imputing)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis)
5. [Bivariate Analysis](#bivariate-analysis)
6. [Multivariate Analysis](#multivariate-analysis)
7. [Conclusion](#conclusion)
8. [Acknowledgment](#acknowledgements)
9. [Contact](#contact)

## Introduction
The goal of this project is to analyze loan data to find patterns and insights. By examining various attributes of the loans, we aim to identify trends and factors that contribute to loan defaults and charge-offs.

## Data Description
The dataset includes the following key columns:

### Based on above column description, below are some of the columns which looks useful and thus are further divided and categorised.

| Customers Location    |
|---------|
| Employment Title (title)  | 
| Employment Length (emp_length)    | 
| Zip Code (zip_code)|
| Description  (desc)| 

<br/>

| Loan Characteristics | 
|---------------|
| Loan Amount (loan_amnt) |
| Funded Amount (funded_amnt) |
| Funded Amount Investment  (funded_amnt_inv) |
| Interest Rate (int_rate) | 
| Loan Status (loan_status) |
| Loan Grade (grade) |
| Loan Issue Date (issue_d) |
| Loan Sub Grade (sub_grade) |
| Income Verification (verification_status) |

<br/>

| Behavior Variables | 
|---------------|
| Delinquency Year -2 (delinq_2yrs)  |
| Debt to income (Dti) |
| Earliest Credit Date (earliest_cr_line) |
| Revolving balance (revol_bal)  |
| Loan Purpose (purpose) |
| Term (term) |
| Annual Income (annual_inc) |
| Employeement Length (annual_inc) |
| Home Ownership (home_ownership) |
| Number of Credit Lines(total_acc) |
| Open Credit Lines (open_acc) |
| Derogatory Record (pub_rec) |
| Record of Bankruptcies (pub_rec_bankruptcies) |
| Revolving Credit Balance(revol_bal) |
| Revolving Utilization Rate (revol_util) |
| Loan Title (title) |

<br/>

| Post Loan Sanction | 
|---------------|
| Total Payment Recieved (total_pymnt)  |
| Investor Payment Received (total_pymnt_inv)   |
| Interest Received (total_rec_int)  | 
| Late Fees Received (total_rec_late_fee)|
| Principal Received (total_rec_prncp) |
| Recovery Fee (collection_recovery_fee)|

## Data Cleaning, Filtering and Imputing
The dataset is cleaned by removing null values and duplicates.
Inconsistent and irrelevant data points are filtered out to ensure the quality of the analysis.
Filtering the data for Current loan status, as its irrelevant for analysis.

## Exploratory Data Analysis
Exploratory Data Analysis (EDA) involves visualizing the data to understand the distribution and relationships between different variables.

## Univariate Analysis
Analysing numerical and categorical data and seeing how each of them behave individually in case of loan defaulter.

### Observations
- Loan Amount: More defaults are happening for loan amount between 5k to 17K, with a mean of 10K. Lets analyse more
- Funded Amount: 5k to 17K 
- Funded Amount Inv: 5k to 17K
- term : default rate is higher 36
- int_rate: 11 to 16%, 13% showing the highest default
- installment : lot of outliers present, default are more between 180 to 420
- emp_length : 0-2 & 10 years more defaulters
- annual_inc : lot of outliers present
- dti : defaulters between 9 to 19 dti
- delinq_2yrs : doesn't show much impact
- mnths_since_last_delinq: delinq_2yrs around 5k records in no delinquency for last 2 years and here we are seeing there is delinquency between 0-20 months as well. Hence delinq data looks incorrect. we can remove them.
- inq_last_6mths: less defaulters if more inquiries, there is a correlation here. Loan given with zero inquiries has highest defaulters.
- open_acc: the chance of default is more if there are credits between 6 to 12
- pub_rec: public derogatory shows no direct impact on defaults, as major default happens with 0 derogatory remarks too
- revol_bal: lot of outliers present.
- revol_util : as the rate increases so does the defaulters, some trend being seen.
- total_acc : more chances of default for credit lines between 11 to 28
- out_prncp : show similar values. can be removed
- recoveris : shows lot of outliers
- collection_recovery_fee : show lot of outliers and looks to be a post charge off formality and can be removed.
- pub_rec_bankruptcies: has no direct impact.
- grade : Major contributers are B, C, D
- home_ownership : Rent and Mortgage is having more have more defaulters. Rent is the leading.
- verification_status : verified and not verified has more contribution in defaulters
- purpose : debt_consolidation has the highest defaulting rate.
- earliest_credit_line : Need more analysis, as the graph shows some trend on the credit line.
- last_credit_date : shows that for one date the defaulter count is more.
- issue_d: shows the trend that from jan to dec 2011 more defaulters were there and especially the graph for issue_year shows more in 2011.
- int_rate : 9-13% and 13-17% are major contributors
- loan amount : 5-10K loan is a major contributer
- annual income: 25-30K is a major contributer

## Bivariate Analysis
Bivariate analysis examines the relationship between two variables to identify patterns and correlations.

### Observations
#### High Charged off or default rates with below combination.
- annual income vs loan_amnt: betwen 30-35K with interest rate between 15 to 17.5 (higher side)
- annual income vs int rate: interest rate between 21-24% and income > 80K. 
- loan amount vs int rate : loan amount between 30-35K and interest rate between 16 to 17.5%
- annual income vs purpose: with home_improvement and annual income between 60 to 80K
- annual income vs home ownership : ownership type Mortgage and income between 70-80K

## Multivariate Analysis
Multivariate analysis explores the relationships between three or more variables simultaneously to uncover more complex patterns.

### Observations
#### Below are the reasons for loan defaulters based on multivariate analysis.
- the term is 36 
- if the grade is B or C
- if the purpose is debt_consolidation 
- home_ownership is RENT or Mortgage
- verification_status is Not Verified
- loan_amount between 5k-10k
- int_rate between 9-17%

## Conclusion
### Combining all the above analysis major reasons for loan defaults are as follows.
- the term is 36 
- if the grade is B or C
- if the purpose is debt_consolidation 
- home_ownership is RENT or Mortgage
- verification_status is Not Verified
- loan_amount between 5k-10k
- int_rate between 9-17%

## Acknowledgements
- This project was inspired by upgrad case study on lending company.

## Contact
Created by [@dsharma3] - feel free to contact me!