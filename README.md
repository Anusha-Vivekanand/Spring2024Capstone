# Spring2024Capstone
Repository for Spring Capstone project

# **Home Credit Default Risk Analysis** </br>
This repository contains a combination of both R (.rmd) and Python (.ipynb) files, Exploratory Data Analysis done in R and Modelling done in python to explore both R and Python for for this data set.
 
# **Table of Contents**
### [Summary of business problem and project objective](#summary-of-business-problem-and-project-objective) </br>
### [Process, solution and business value](#process-and-solution) </br>
### [Challenges](#challenges) </br>
### [Learnings](#learnings)



### Summary of business problem and project objective
Many people struggle to get loans because they either have a short credit history or none. Unfortunately, some lenders take advantage of these individuals. Home Credit wants to help by making it easier for these people to borrow money in a safe and positive way. They use alternative data, from Telco and Transactional information, to predict if clients can repay loans using machine learning and statistical approaches. Home Credit is looking for new ideas to improve their predictions and make sure more people who can repay get approved for loans. They also want the customers who have potential to repay loans to not be rejected from being offered a home loan while providing in detail repayment calendar containing principal and maturity information of the loan so that customers are better informed.

These are the benefits of the solution: </br>
1.Enhanced prediction accuracy ensures deserving clients who are capable of repaying are not rejected. </br>
2.Provides a secure and positive borrowing experience while reducing the risk of exploitation by untrustworthy lenders. </br>
3.Empowers clients with loans tailored to support their financial success.

The analytics approach encompasses leveraging statistical and machine learning techniques, including supervised learning and classification models. Specifically, we aim to enhance Home Credit's credit scoring system by extracting insights from telco and transactional data and building a predictive model that provides a comprehensive list of customers who can repay the loan.

This project will be a success if the people who can repay the loan are offered the loan based on our prediction model. This will help in not rejecting good candidates with repayment capacity. As noted, this project is focused on prediction. Therefore, we will not be including any analysis of why customers are failing to repay the loan. That analysis is out of scope for the current project.

### Process, solution and business value
To run the .rmd file the following libraries are required to be installed : </br>
dplyr, readr, tidyverse, ggplot2 </br>
To run the .ipynb file the following libraries are required to be installed through either 'conda intall library name' or 'pip intall library name' : </br>
warnings, numpy, pandas, matplotlib.pyplot, seaborn, sklearn.model_selection, sklearn.preprocessing, xgboost, sklearn.model_selection, sklearn.linear_model, sklearn.ensemble </br>

Application Train dataset had information of customer's credit application. There is an important column called TARGET that is a binary flag which says 0 or 1 based on if the customers have issues paying back the loan or not. </br>

While data cleaning , We incorporated null value treatment for categorical columns and numerical columns separately. The methodologies used were Mode imputation for object columns because here we had the count of occurances in each column, median imputation for numeric columns because imputation of mean can cause skewing when an outlier is present. For the values that could not be substitued we have eliminated the columns.
During EDA we were able to create hypotesis on variables like gender, Age, Occupation type and other univariate and multi variate analysis on the given dataset. </br>

My particular contribution was to create pre modelling techniques and feature engineering because based on the priliminary EDA I was able to find that there were 91.92% of the customer base that did not having issue in repaying the loan. On further investigation I was able to find that this is due to class imbalance were 282,686 customers had the binary flag corresponding to no issues to repay while 8.07% (24,825) customer base had issues paying back the loan. This issue was dealt by balancing out the classes before create our models. I was also able to create a random forest model that was able to give us an accuracy score of 0.68. I was able to support my team with debugging any code chunk wherever required. </br>

Apart from this the group was able to create 2 more models of Logistic Regression and XGBoost where income , occupation type andn loan type were the top predictors. </br>

Since employment and income are top predictors the business should concentrate on lending loans based on different interest rate range for these 2 criteria. </br>

### Challenges

One of the challenges was the dataset cleaning for a huge dataset which had to be dealt with column elimination for most of them and thus impacting KPI selection. Since a lot of categorical variables were present , identifying individual columns for one hot encoding was a challenge. This was crucial as this was the input for building models.

### Learnings

I had both technical and collaborative learning through this project. I had an opportunity to explore both R and Python in the same datasets and was a good practise to brush up my coding skills. I was able to learn to collaborate and brain storm ideas with my team which was a very good interpersonal skill development in the project.
