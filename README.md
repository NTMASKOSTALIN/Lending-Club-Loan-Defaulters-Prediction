# Lending-Club-Loan-Defaulters-Prediction

# Introduction
LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC), and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.

Solving this case study will give us an idea about how real business problems are solved using EDA and Machine Learning. In this case study, we will also develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

# Business Understanding
You work for the LendingClub company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company
The data given contains the information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for takin actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.

When a person applies for a loan, there are two types of decisions that could be taken by the company:

Loan accepted: If the company approves the loan, there are 3 possible scenarios described below:
Fully paid: Applicant has fully paid the loan (the principal and the interest rate)
Current: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.
Charged-off: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan
Loan rejected: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

# Business Objectives
LendingClub is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface.
Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). The credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who defaultcause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.
If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA and machine learning is the aim of this case study.
In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.
To develop your understanding of the domain, you are advised to independently research a little about risk analytics (understanding the types of variables and their significance should be enough).

# Data Description
Here is the information on the particular dataset:

| # | LoanStatNew | Description |
|---:|---|---|
| 0 | `loan_amnt` | The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, it will be reflected in this value. |
| 1 | `term` | The number of payments on the loan. Values are in months and can be either 36 or 60. |
| 2 | `int_rate` | Interest rate on the loan. |
| 3 | `installment` | The monthly payment owed by the borrower if the loan originates. |
| 4 | `grade` | LendingClub-assigned loan grade. |
| 5 | `sub_grade` | LendingClub-assigned loan subgrade. |
| 6 | `emp_title` | The job title supplied by the borrower when applying for the loan. |
| 7 | `emp_length` | Employment length in years. Possible values are between 0 and 10, where 0 means less than one year and 10 means more than 10 years. |
| 8 | `home_ownership` | The home ownership status provided by the borrower during registration or obtained from the credit report. Values include RENT, OWN, MORTGAGE, and OTHER. |
| 9 | `annual_inc` | The self-reported annual income provided by the borrower during registration. |
| 10 | `verification_status` | Indicates if the income was verified by LendingClub, not verified, or if the income source was verified. |
| 11 | `issue_d` | The month which the loan was funded. |
| 12 | `loan_status` | Current status of the loan. |
| 13 | `purpose` | A category provided by the borrower for the loan request. |
| 14 | `title` | The loan title provided by the borrower. |
| 15 | `zip_code` | The first 3 numbers of the ZIP code provided by the borrower in the loan application. |
| 16 | `addr_state` | The state provided by the borrower in the loan application. |
| 17 | `dti` | A ratio calculated using the borrower's total monthly debt payments on total debt obligations, excluding mortgage and the requested LendingClub loan, divided by the borrower's self-reported monthly income. |
| 18 | `earliest_cr_line` | The month the borrower's earliest reported credit line was opened. |
| 19 | `open_acc` | The number of open credit lines in the borrower's credit file. |
| 20 | `pub_rec` | Number of derogatory public records. |
| 21 | `revol_bal` | Total credit revolving balance. |
| 22 | `revol_util` | Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit. |
| 23 | `total_acc` | The total number of credit lines currently in the borrower's credit file. |
| 24 | `initial_list_status` | The initial listing status of the loan. Possible values are W or F. |
| 25 | `application_type` | Indicates whether the loan is an individual application or a joint application with two co-borrowers. |
| 26 | `mort_acc` | Number of mortgage accounts. |
| 27 | `pub_rec_bankruptcies` | Number of public record bankruptcies. |

