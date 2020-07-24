## David_Portfolio

Example Data Science Portfolio

# [Project 1: Bankruptcy Prediction: Project Overview](https://github.com/sd2beatles/portfolio_polish_bankruptcy)

Data Science Portfolio (1) Bankruptcy-prediction-in-Polish-Comapnies
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


# [Project 3: Naver Sentimental Movie]

### 1) Intorudciton 
This is a movie review dataset in the Korean language. Reviews were scraped from Naver Movies.
The dataset construction is based on the method noted in Large movie review dataset from web scraping 

- Each file is consisted of three columns: id, document, label

    id: The review id, provieded by Naver
    document: The actual review
    label: The sentiment class of the review. (0: negative, 1: positive)
    Columns are delimited with tabs (i.e., .tsv format; but the file extension is .txt for easy access for novices)

### 2)Characteristics

   - All reviews are shorter than 140 characters
   - Each sentiment class is sampled equally (i.e., random guess yields 50% accuracy)
        100K negative reviews (originally reviews of ratings 1-4)
        100K positive reviews (originally reviews of ratings 9-10)
        Neutral reviews (originally reviews of ratings 5-8) are excluded
  

