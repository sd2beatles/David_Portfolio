## David_Portfolio



# [Project 1: Distressed Companies Classification:Project Overview](https://github.com/sd2beatles/DATA-SCIENCE-PROJECT_FINANCE)
Still in progress


### 1. Introduction (시작)

The covid-19, a catastrophic event around the world,  swapped the financial market, bringing out an unprecedented level of chaos to all parties in the market. To reduce the huge impact on ordinary citizens, the federal government decided to lower its real interest rate up to 0.0%. The initial aim was to bring vitality to the entire economy, but on the other side, this leads in turn to harm the constructive economy in some manner. One of the adversities is to allow endurance to companies that were supposed to have been expelled from the market. Just think how horrible it is for 'naive' people to invest their funds into the 'zombie' firms. 

코로나로 인해 시장이 제 역할을 하지 못하고 혼돈의 시간을 보내고 있었으며, 미국 중앙은행은 서민들의 막대한 피해를 줄이고자 실질 금리를 0% 까지 내리는 급단적인 대처방안을 내놓게 됩니다. 이에 따라 시장의 성장성이 이미 멈춰서 퇴출에 놓인 회사들은 낮은 이자율로 인해서 수명을 연장을 할 수 있게 되었습니다. 이러한 재무적으로 건강치 못한 회사들에 투자하게 된다면, 모든 피해들은 고스란히  '순진한'투자들에게 돌아가게 됩니다. 그렇다면 이러한 회사들을 완전히 배제할 수는 없겠지만, 어느 수준까지는 머신러닝 기법의 알고리즘을 통해서 거를 수 있지는 않을까하는 생각에 이 프로젝트를 진행하게 됩니다. 



금융위원회는 지속적으로 금융거래가 정지된 회사와 관리종목들을 지속적으로 모든 투자들에게 제공하고 있습니다.이러한 목록에 속한 종목들과 재무제표정보를 네이버 금융에서 얻을 수 있습니다. 다만 네이버는 금융정보에 대한 api를 제공하지 않으므로, 모든 종목들을 web-scaping(웹크롤링)하도록 하겠습니다. 




### 2. Sections (목록)


![image](https://user-images.githubusercontent.com/53164959/115359896-1324b200-a1fa-11eb-8019-aa162be2a376.png)




![image](https://user-images.githubusercontent.com/53164959/115405119-ed62d180-a228-11eb-960d-b591e57a8c2b.png)







# [Project 2: Bankruptcy Prediction: Project Overview](https://github.com/sd2beatles/portfolio_polish_bankruptcy)
:thumbsup: Completed

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


# [Project 3: Data Analysis For Brazil E-commerce: Project Overview](https://github.com/sd2beatles/Brazil_Ecomerce)
:thumbsup: Completed


- Prepared a variety of charts to help merketers to handle with some of issues the company has experienced.
- Data was retrieved from Kaggle. The link is as follows;  [https://www.kaggle.com/olistbr/brazilian-ecommerce]
- Mathcing Products Based On Euclidean Distance, KNN, Iterative Imputation, PCA,Poission Regression,and Isolaton Forests Used to preprocessing data

<img src='https://user-images.githubusercontent.com/53164959/86457594-df59c800-bd5e-11ea-8f9f-7bd8d29a9ab4.png' alt="Drawing" style="width: 50px;"/>

# [Project 4:Log Data Analysis(Excessive Use of SQL)](https://github.com/sd2beatles/log_data_analysis)
:thumbsup: Completed

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
:thumbsup: Completed

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



