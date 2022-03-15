## David_Portfolio

# [Project 1: 학원 수강생 관련 데이터 생성/적재/분석/모델링 (전과정)](https://github.com/sd2beatles/Student_transaction)
:thumbsup: complete

## 1) Objective

전 직장에서 자주 봤던 회사 내부의 로그파일들의 유사한 형태로 데이터를 생성시켜, 이를 토대로 주어진 공간에 적재 및 모델링을 하는 것이 주 목표입니다.

## 2) Tool Sets

- Operating System: WSL2 Unbuntu 
- Program Language: Python3.8
- Big Data Tool: Pyspark 3.0.1
- Workflow: Apache Airflow
- Cloud System: AWS (S3,Dynamodb,Athena)
- Docker
- Jupyter Notebook


## 3) Method

### 3.1 Generate Student Transaction

학생들의 각 각의 자료들은 크게 세 가지로 구분되어 있습니다.

    - 수강생의 인적 사항     
    - 수강생의 수강 구매 기록 
    - 수강생의 온라인 로그인 기록
    
  각각의 자료를 생성할 수 있는 simulator를 generator 폴더 안에 저장되어 있습니다. 각 생성된 자료들은 내부 디스크 또는 aws s3로 전달될 수 있게 설정을
  해놓았습니다. 더 자세한 정보는 /home/david/airflow/generator/Utils/Config/parser.py을 살펴보시면 될거 같습니다. 예를 들어 내부 디스크 안에 
  기록을 저장하고 싶다면,아래와 같이 설정하시면 됩니다. 만약 생성된 자료가 많을 시에는 병렬처리 프로그램도 설정을 해놓았기 때문에,cpu의 갯수와 적절한
  config를 설정하시면 <b>Parallelism</b>으로 데이터의 생성 속도를 빠르게 증진시킬 수 있습니다. 
  
  ```sh

  python generate_transactions.py \
--json_input    <input_space> \
--output_path   <output_path> --is_logging True
  ```
 위의 명령으로 인해 다음과 같은 출력을 얻을 수 있습니다. 
 
  ```txt
  /usr/transaction/data/demo/20220312/loginApp.log:72393:[[]]-UserId:nross=Action:add_cart SUCCESS ShortSession:e57b8710 LongSession:91b3d5bb2b31 [loginApp] VisangEduDuo transaction:[product_code:ckrkr05,amtmt06,amount:675000,time_stamp:2022-01-24:04:33]-URL:https://www.visangstudy.com?utm_source=htts://www.facebook.com&utm_medium=banner&utm_campaign=monthly_promotion&utm_term=논술 Path:/search_list?search_=mt03-m1-fundamental

/usr/transaction/data/demo/20220312/loginApp.log:70543:[[]]-UserId:nross=Action:add_cart SUCCESS ShortSession:6228dd42 LongSession:a9719df6e03f [loginApp] VisangEduDuo transaction:[product_code:benen01,amtmt02,amount:359000,time_stamp:2022-01-22:19:44]-URL:https://www.visangstudy.com?utm_source=https://www.twitter.com&utm_medium=cpc&utm_campaign=semeter_start_sale&utm_term=모의 고사 준비 Path:/search_list?search_=sc02-m1-intermediate
```
  
  ### 3.2 Load and Processed Data 
  
 이렇게 축척된 데이터를 s3 또는 내부에 지정된 곳에 저장하셨다면, raw data를 전처리를 해야합니다. 이때, airflow를 이용하며, 각각의 task가 잘 진행되는지
 체크할 수 있습니다. 
 
 ![image](https://user-images.githubusercontent.com/53164959/158401328-3a56c52d-b24d-4e65-be74-36f4a2982e5c.png)
 
 
 
 ### 4. Data Ananysis 
 
Pysparkf를 통해서 두 번째 전처리를 진행한 후에, 데이터 분석을 진행합니다. 자세한 내용은 transaction_pyspark.ipynb를 확인해 주세요. 

![image](https://user-images.githubusercontent.com/53164959/158402041-737670b7-df34-424d-8b8e-af9783ce90c5.png)


### 5. Modeling 

마지막으로 Modeling을 통해서, 각 학생의 평균적인 로그인 시간(즉 수강시간)을 예측해 봅니다. 자세한 내용은 transaction_modeling.ipynb를 확인해 주세요. 



### 6. Verision 

아직까지 첫 버전이라서 오류가 많을거라 사료됩니다. 일을 하면서 만든  개인 적인 포트폴리오라 시간도 많이 들었고, 서툼점도 많습니다.지속적인 update를 통해서 더 나은 버전을 만들어 보겠습니다. 긴 글 읽어주셔서 감사합니다. 

  

  


# [Project 2: Sale-Prediction:Data Competition](https://github.com/sd2beatles/Sale-Prediction)

:thumbsup: complete

# Sale-Prediction (Ranked 4th)


## :globe_with_meridians: Introduction 



In this competition I was working with a challenging time-series dataset consisting of daily sales data, kindly provided by stores in Koarea. To predict total sales for every product and store in the next month. By solving this competition I was able to apply and enhance your data science skills. I was ranked 4th in the competition. 

#### According to the agreement, a full discolue of contents is forbidden.Because I have excluded all the private infomration on the clients,the dimension of transformed data is much smaller than that of the original data.




## :globe_with_meridians: Steps

- Part 1: Collection of Data From  API
  - Creating a database and tables for data storage
  - Choosing one of the two given formats; 
    - Pandas DataFrame (python3)
    - MySQL 

- Part 2: Build up Amazon Web Services RDS 
  - Connecting to a DB instance running the MySQL databse engine

- Part 3: Modeling
  
  -Light GBM has demonstrated the best performance. 
  


## :globe_with_meridians: Special Notes

:pencil2:  _AWD RDS(Amazon Relational Database Service)_

In order to connect to Database instance, we need to first obtain an endpoint and port value from the AWS Management Console. 
Right after acquisition of the information, we are now able to connect to a DB instance using MySQL client by typing the below command line. 

```sql
mysql -h endpoint -P port_number -u masteruser -p
```



# [Project 3: Distressed Companies Classification:Project Overview](https://github.com/sd2beatles/DATA-SCIENCE-PROJECT_FINANCE)
:thumbsup: complete



### 1. Introduction 

The covid-19, a catastrophic event around the world,  swapped the financial market, bringing out an unprecedented level of chaos to it.To minimize the huge impact on every part of econonmy,the federal government immediately decided to lower its real interest rate up to 0.0%. The initial aim was to bring vitality to the entire economy, but on the other side, this caues many unwanted problmes. One of the adversities is to allow endurance  to companies that were supposed to have been expelled from the market. The highly leveraged firms should keep afloat in the ‘sea’ for temporary but are  more likely to be the shock ‘amplifiers’ if the central bank keep the redemption closed. The real 
problems kicked in as disaster relief was made to all citizens regardless of their income level. Even though many households lived off the temporary subsidies, a considerable portion of the support went to the financial market. The real problem comes along with it. According to the research paper issued by Hana Bank in South Korea, it reports that those whose average of period of investing is less than 6 months lost a half of their initial deposits and almost 60 % of 
them have not used the financial statements for their investing decisions. This gives me a motivation to build a machine learning model which classify a company into two 
statuses either distressed or running.

More details on problems statements and methodologies are provided in the project proposal and check out the linked below.

https://github.com/sd2beatles/DATA-SCIENCE-PROJECT_FINANCE/blob/main/analysis/project%20propsal.pdf


### 2. Requirements


- Python 3.6+ 
- pytorch
- pykrx  (collecting information on the companies listed on the stock exchange in South Korea)
- Wokrs on Linux(Ubuntu)

### 3. Steps to Collect Data

First, we need to obtain the list of companies that are either currently or ceased to be listed on the stock exchange. All the lists can be obtained through pykrx and NAVER. Make sure that you have  pykrx library installed in advance. 

Second, the acquisition of the unique code for each firm is now followed by sending a valid access token in the request header.  
Apparently, the first two steps look a little complicated, but all the information can be automatically acquired by entering the following code in your terminal. Double check if the file containing a name and its unique code is created in the designated path. 


```unix
python loadCompanyList.py --key auth-token --output output-path 
```

Lastly, all the finanacial information of the listed comapnies are stored as the separate file. 

```unix
python loadData.py --key auth-token --input file_path_containing_code --output file_path_storing_financial_summary 
```

### 4. Preprocessing Data and Exploratory Data Analysis 

For our classifiers to work, we need to feed data into a format that could be computed upon. Right after the transformation, we need to gain a much deeper understanding of the overall picture of the financial structure of companies.  All the codes to run the tasks are witten in the Jupiter notebook.  

https://github.com/sd2beatles/DATA-SCIENCE-PROJECT_FINANCE/blob/main/analysis/Preprocessing%2CDataAnalysis%2CCharts.ipynb

![image](https://user-images.githubusercontent.com/53164959/125382591-e20ae680-e3d0-11eb-9178-8f64042721fd.png)


### 5. Machine Learing Algorithms Used for The Classification 

- DBSCAN ( removing outliers) 
- Isolaton Forest ( removing outliers)
- PCA (dimesional reduction)
- Logistic Regression (classification)
- Kernal Support Vector Machine(classfication)
- K-nearest Classifier(classification)
- Random Forest(classfication)
- Naive Bayes(classfication)
- Light GBM(classfication)

### 6. Final Report

https://github.com/sd2beatles/DATA-SCIENCE-PROJECT_FINANCE/blob/main/analysis/Final%20Report.pdf









# [Project 4: Data Analysis For Brazil E-commerce: Project Overview](https://github.com/sd2beatles/Brazil_Ecomerce)
:thumbsup: Complete


- Prepared a variety of charts to help merketers to handle with some of issues the company has experienced.
- Data was retrieved from Kaggle. The link is as follows;  [https://www.kaggle.com/olistbr/brazilian-ecommerce]
- Mathcing Products Based On Euclidean Distance, KNN, Iterative Imputation, PCA,Poission Regression,and Isolaton Forests Used to preprocessing data

<img src='https://user-images.githubusercontent.com/53164959/86457594-df59c800-bd5e-11ea-8f9f-7bd8d29a9ab4.png' alt="Drawing" style="width: 50px;"/>

# [Project 5:Log Data Analysis(Excessive Use of SQL)](https://github.com/sd2beatles/log_data_analysis)
:thumbsup: Complete

![image](https://user-images.githubusercontent.com/53164959/88487467-4c5c2880-cfc0-11ea-8d4d-05aad5cf29bb.png)


1) Introduction

Online business is now enjoying an unprecedented level of popularity compared to the last decade. However, every online business has steps that people must take to become a customer.  The people who simply visit the sites are not customers, but sign up for your online service or purchase a product from your website. Therefore, to take a very in-depth look into how consumers behave is an essential task every analyst should take.  

2) Goal and Project

It is my first time to manage the pretty a large size of data with excessive use of SQL queries for data analysis. Although Pandas, one of the Data Frame libraries provided by Python, might have been deployed to analyze the data-set, it takes much longer to process the queries for ceratin tasks than under SQL. I decide to take a combination of both programs for the convenience. ( Almost 80 % of data has been performed using SQL queries)

3) Data 

Detailed infomration regarding the data can be checked out from the following website. https://www.kaggle.com/c/ga-customer-revenue-prediction/data

4) Program Uses

Python(version 3.7.0) and Postgresql



# [Project 6: Bankruptcy Prediction: Project Overview](https://github.com/sd2beatles/portfolio_polish_bankruptcy)
:thumbsup: Complete

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

  
# [Project 7: Human Activity](https://github.com/sd2beatles/humanActivity)
:thumbsup: Complete

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



