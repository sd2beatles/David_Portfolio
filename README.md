## David_Portfolio

Example Data Science Portfolio

# [Project 1: Bankruptcy Prediction: Project Overview](https://github.com/sd2beatles/portfolio_polish_bankruptcy)


### 1) Data Summary

Based on the certain measures (around 64) we predict the health of the company like whether it will go ahead or will it go Bankrupt

Bankruptcy prediction is the art of predicting bankruptcy and various measures of financial distress of public firms. The importance of the area is due in part to the relevance for creditors and investors in evaluating the likelihood that a firm may go bankrupt. It is a vast area of finance and accounting research.

Detailed infomration regarding the data can be checked out from the following website. https://www.kaggle.com/squintrook/forecasting-bankrupts-with-ann

### 2) Goal and Obejective

To construct a model with the fewest input factors but higher accuracy.

### 3) Structures

The major part of project 1 focuses on intensive analysis of each given factor. Also, the data itself is highly susceptible to outliers, which makes me spend a great deal of time filtering out those extreme values.

Part 2 specializes in constructing a model with chosen factors from part 1 for classification. With the 8 chosen factors, I have achieved an accuracy of 99%.

![image](https://user-images.githubusercontent.com/53164959/88418989-5b57a500-ce1f-11ea-9d1b-2e68fe95210d.png)


# [Project 2: Data Analysis For Brazil E-commerce: Project Overview](https://github.com/sd2beatles/Brazil_Ecomerce)

- Prepared a variety of charts to help merketers to handle with some of issues the company has experienced.
- Data was retrieved from Kaggle. The link is as follows;  [https://www.kaggle.com/olistbr/brazilian-ecommerce]
- Mathcing Products Based On Euclidean Distance, KNN, Iterative Imputation, PCA,Poission Regression,and Isolaton Forests Used to preprocessing data

<img src='https://user-images.githubusercontent.com/53164959/86457594-df59c800-bd5e-11ea-8f9f-7bd8d29a9ab4.png' alt="Drawing" style="width: 50px;"/>

# [Project 3:Log Data Analysis(Excessive Use of SQL)](https://github.com/sd2beatles/log_data_analysis)


![image](https://user-images.githubusercontent.com/53164959/88487467-4c5c2880-cfc0-11ea-8d4d-05aad5cf29bb.png)


1) Introduction

Online business is now enjoying an unprecedented level of popularity compared to the last decade. However, every online business has steps that people must take to become a customer.  The people who simply visit the sites are not customers, but sign up for your online service or purchase a product from your website. Therefore, to take a very in-depth look into how consumers behave is an essential task every analyst should take.  

2) Goal and Project

It is my first time to manage the pretty a large size of data with excessive use of SQL queries for data analysis. Although Pandas, one of the Data Frame libraries provided by Python, might have been deployed to analyze the data-set, it takes much longer to process the queries for ceratin tasks than under SQL. I decide to take a combination of both programs for the convenience. ( Almost 80 % of data has been performed using SQL queries)

3) Data 

Detailed infomration regarding the data can be checked out from the following website. https://www.kaggle.com/c/ga-customer-revenue-prediction/data

4) Program Uses

Python(version 3.7.0) and Postgresql



  
# [Project 5: Human Activity](https://github.com/sd2beatles/humanActivity)

![image](https://user-images.githubusercontent.com/53164959/88954047-c0eeda00-d2d4-11ea-9514-f4352d265a7c.png)


# 1. Introduction
humanActivity

Human Activity Recognition (HAR) using smartphones dataset and an LSTM RNN. Classifying the type of movement amongst six categories:

WALKING,
WALKING_UPSTAIRS,
WALKING_DOWNSTAIRS,
SITTING,
STANDING,
LAYING.
Compared to a classical approach, using a Recurrent Neural Networks (RNN) with Long Short-Term Memory cells (LSTMs) require no or almost no feature engineering. Data can be fed directly into the neural network who acts like a black box, modeling the problem correctly. Other research on the activity recognition dataset can use a big amount of feature engineering, which is rather a signal processing approach combined with classical data science techniques. The approach here is rather very simple in terms of how much was the data preprocessed.

Let's use Google's neat Deep Learning library, TensorFlow, demonstrating the usage of an LSTM, a type of Artificial Neural Network that can process sequential data / time series.

# 2. Problem Statemet

Given a new datapoint we have to predict the Activity

# 3. Methods

Models used: LSTM,Support Vector Machine,and  XG boost 
Grapical Visualizaiton: Tableau
Programming : Python(Version 3.7.0) and Jupyter Notebook


# 3. Test reutls 

Note that all the peformanace measures are based on F-1 scores. 

- Support Vector Machines: 96 % 

- LSTM: 92 %

- Xgboost : 94 %



