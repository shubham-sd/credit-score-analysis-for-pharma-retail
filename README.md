# Credit Score Analysis for Retailers in Pharma-Retail Industry

* The purpose of this document is to outline the high-level design of the “CREDIT SCORING FOR RETAILERS” and provide an overview for the tool implementation.
* CREDIT SCORING FOR RETAILER  is  an application which gives the better understanding of the business and provide a better insights for the valuable customers.

# Data Collection and Business Understanding

* Data has been obtained from secondary source.
* Data provided to us is related to the pharmaceutical industry and it is related to the retailers and their bill amount.
* We had to perform RFM analysis on the provided data and we have to give the credit score to the retailers.
* Data is extracted from MYSQL database to python using MYSQL Connector library providing server, database and table name.
* Data has many noise like null values and outlier.

## Tech Stack

**Tech Used:** Vs Code for working on models, Jupyter Notebook, 
Postgresql, Python, Streamlit

**Libraries Used:** ***Pandas*** for Data Manipulation, ***matplotlib*** 
and ***seaborn*** for data visualizaiton, ***make_pipe*** for making pipeline, 
***column_transformer*** for encoding data before training ***sklearn*** for data preprocessing 
and model building, ***Streamlit*** for web application, and ***heroku*** for deployment.

## EDA and Data Preprocessing

* Some imputations and typecasting was done
* RFM was performed on the data and reduced some columns to only Recency, Frequency and Monetary 
* Clustering was done to group same customers/retailers

## Model building
In order to get the best accuracy following models were used:

    1. Random Forest Classifier
    2. Support Vector Machine Classifier (rbf and poly)
    3. KNeighbours Classifier 
    4. Gausian Naive Bayes Classifier

Out of which Gausian Naive Bayes Classifier performed well with test accuracy of 90% 
and train accuracy of 91% and pickled for model deployment.

## Model deployment
Model was deployed on Heroku.

Deployment link:- https://credit-analysis-for-retailers.herokuapp.com/
