# LOAN APPROVAL SYSTEM

Aim of this project was to create a model that trains on a set of loans to invest in and categorize them as DEFAULT or NOT. There are many ways to achieve this but for the purposes of this problem, we decided to create models based on a loan database of clients to predict whether a loan is worth investing in or not.

## Data Preparation

Data from SOURCE: [https://www.lendingclub.com](https://www.lendingclub.com/)was obtained to use in the project. (LendingClub is an American peer-to-peer lending company, headquartered in San Francisco, California. At its height, LendingClub was the world&#39;s largest peer-to-peer lending platform. LendingClub enabled borrowers to create unsecured personal loans between $1,000 and $40,000. The standard loan period was three years. Investors are able to search and browse the loan listings on LendingClub website and select loans that they wanted to invest in based on the information supplied about the borrower, amount of loan, loan grade, and loan purpose. Investors made money from the interest on these loans. LendingClub made money by charging borrowers an origination fee and investors a service fee.)

#### Redundant Data

Dataset contained many redundant data which was removed. Features without any information were also removed to better understand the dataset.

#### Missing Data

A few of the predictors that we had selected had significant missing data. We had two options when dealing with this problem. Either eliminate the loans, or impute a value. We decided to impute values whenever possible in order to make sure that we were not systematically eliminating loans from our analysis and then eliminated the rest of the data.

#### Outliers

To deal with outliers, we only considered complete loans that were either paid off or charged off.

#### Design Matrix

We included in our design matrix only those features that were available to borrowers on the Lending Club website. The data was scaled. This improved our results. Categorical values such as home ownership, income validation, Address etc were encoded with one-hot-encoding.

## EDA

### Loan Distribution

CDF showing loan distribution

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture1.png)


### Loan Status

Types of Loans based on their final status(Paid vs Default)

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture2.png)

###


### Loan Purpose

Purpose for which Loan was obtained

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture3.png)

### Borrowers Employment:

Borrowers with following employments obtained the highest number of loans.

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture4.png)

##


## **Algorithms &amp; Machine Learning**

Python scikit was used for training the recommendation system. Datasets were tested on the different algorithms provided, and every time the Random Forest Classifier algorithm performed the best. It should be noted that this algorithm, although the most accurate, is also the most computationally expensive.

### Classification Report

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture5.png)

### ROC Curve Comparison:

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture6.png)

### Model Comparison(True vs Predicted)

Comparison of models based on True vs Predicted value:

![](https://github.com/errorcode007/Lending_Club_Capstone/blob/main/Picture7.png)

## **Future Improvements**

A new parameter could be introduced which could take in consideration the profits and loss from the sets of loan applicants and then by providing a risk factor on the net profit we could use it to approve lenders for better risk management from a list of several applicants to minimize loss.
