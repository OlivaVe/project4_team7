# Are Credit Approvals influenced by Demographics?

## Why Do We Choose Our Topic?
The decision to embark on the Credit Card Approval Prediction project was driven by a combination of curiosity and real-world relevance. The project holds practical significance in the financial industry. Accurate credit risk assessment not only safeguards lenders against defaults but also ensures that creditworthy individuals gain access to essential financial services.
## Our data set
Our dataset contains several key columns that play an important role in our analysis:
- Gender: Understanding gender dynamics in creditworthiness assessment can reveal important patterns and trends.
- Ownership of Car and House: These factors can reflect an individual's financial stability and capacity to meet credit obligations.
- Number of Children & Family Count Members: Family size can influence financial responsibilities and, consequently, creditworthiness.
- Amount of Income: Income is a fundamental determinant of credit eligibility and repayment capacity.
- Family Status: Family status provides additional context about an individual's financial situation and responsibilities.

In order for us to be able to work with this dataset we had to do some modifications as part of an ETL process:

1. We had the data split into 2 documents so we needed to read these files from an AWS s3 bucket, convert them into a pandas DataFrame and merge them together into a new DataFrame.
2. Then we needed to eliminate unnecessary columns and change the ones that we needed from strings into floats.
3. We also modified two columns ['FLAG_OWN_REALTY' , 'FLAG_OWN_CAR'] that were as Yes or No into binary combinations for easier lecture.
4. We had columns ['DAYS_EMPLOYED' , 'DAYS_BIRTH'] that where expressed in days, so we need to convert them into years. We converted them by dividing by 365.25.
5. We finally changed some column names for easier use.

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/6228ed22-a83a-4d00-9acc-0f57a147b25a)
![image](https://github.com/OlivaVe/project4_team7/assets/127780305/0d6785a3-9011-4300-8f02-e6bff40320ad)


## Models
### Data Preprocessing
In order for us to be able to use our entire dataset, we needed to change some categorical variables into numerical with the help of dummy variables. 

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/6d1d15d2-b250-41c6-a589-176afdb5479a)

In addition to that we needed to divide the dataset into the test data and the trained data, just after that we were able to Standarize the values using the StandardScaler function.

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/319fb603-20e1-4694-ae8d-ee222a0880bd)

We explored various architectural configurations and hyperparameters. Our approach involved the creation of four distinct models, each with carefully modified attributes, aimed at enhancing our predictive power. 

We started with a model that was using all of our 30 features available.

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/5049228d-6f0c-4d82-8b5a-5516d3d5e578)

As we got a really big number in the Accuracy model, we decided to check if it was a case of overfitting, so we decidede to include a RandomForest into the mixture to be able to identify the most influential features of our dataset and see if it would improve our model Accuracy.

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/1a38fbd5-538a-4d18-b6ac-bb7ccfd3740a)

We modified the quantity of layers, optimizer selection, activation function variations, fine-tuning of neuron quantities and training epochs. These meticulous adjustments collectively contributed to the enhancement of our Credit Card Approval Prediction model's accuracy and reliability.

At the end, after 4 different models with different paramenters, we got the following results:

![image](https://github.com/OlivaVe/project4_team7/assets/127780305/13480a62-0fca-47f1-a1b3-bdaee0a41fe4)

## Results
We achieved remarkable results. While the accuracy of all models was good, the highest accuracy we attained was 98.51%. This means that our predictive power in assessing credit card approval significantly improved through careful model architecture selection, hyperparameter tuning, and optimization.

In addition to our predictive model, we decided to do some internal digging of our dataset to see how the approval rate changes with different demopgraphic parameters.

Here is our full tableau project: https://public.tableau.com/views/Project4_team7/Story1
## Conclusion
Our project not only seeks to develop an accurate predictive model but also aims to uncover hidden insights within these crucial dataset columns. By harnessing the power of data science, machine learning, and statistical analysis, we aspire to empower credit card companies with the tools they need to make informed and equitable lending decisions. 

## LINK TO OUR FULL CODE IN GOOGLE COLAB

https://colab.research.google.com/drive/1Wi8PZy_lvLH_RZFDXy9EYxv7S14Bi44M?usp=sharing
