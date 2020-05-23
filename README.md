# Comunicate Data Findings-Prosper Loan
## by Pengfei Huangfu
## Dataset Overview
the dataset contains 113,937 loans with 81 variables. it is very hard and time consuming to figure out what the main features of interest by testing all variables one by one. Based on common sense and my experience in finance, I found that some features are more interesting than others. in this project, I mainly focus on Borrower APR, Prosper Score, Original Loan Amount, Borrower Occupation, Borrower State, Borrower Employment Status and some other feature if it can be used as predictors later on. 

The dataset can be download here: https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1547358770029000

## Summary of findings
### Univariate exploration
my univariate exploration starts from Borrower APR. it is interesting to see that the distribution of Borrower APR is right skewed and there is one spike around 0.36. there are no need to perform any transformation here.
when i plot the distribution of stated monthly income, i found that thre are some outliers which are very far away from the mean. therefore, i log scaled the stated monthly income. and the loged version looks normal distributed.
it is make sense that the most frequent group of people who borrowed loan are employed people.

### Bivariate exploration
i noticed that lender Yield is strongly related to Borrower APR, a higher Lender yield leads to a higher Borrower APR.
The Prosper Score is negatively related to both borrower APR and Lender Yield. a higher credit rating leads to a lower borrower apr and Lender Yield.
loan riginal amount is gegatively related to borrower APR, but the coefficient shows that the relationship is weak.

### Multivariate exploration
firstly, i investigate the relationship among BorrowerAPR, Prosper Score and LoanOriginal Amount and find that larger original amount of loan are taken by people with higher rating.
secondly, i checked the relationship among different type of employment, borrower APR and ProsperScore and find that employed people tend to have higher credit rating and lower borrower APR than unemployed people.

it is suprising to see retired people also have a relatively high borrower APR even though some of them may have good rating.

## key Insights
1.Full-Time and part-time tend to have higher ProsperScore and lower BorrowerAPR
2.Not-Employed & Self-Employed tend to have lower ProsperScore and higher BorrowerAPR
3.loans with larger amount are taken by people with higher credit rating.
4.as the Prosper score goes up, the borrower APR goes down.
5.it is suprising to see retired people also have a relatively high borrower APR even though some of them may have good rating.

