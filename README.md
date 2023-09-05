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
![image](https://github.com/OlivaVe/project4_team7/assets/127780305/0d6785a3-9011-4300-8f02-e6bff40320ad)
![image](https://github.com/OlivaVe/project4_team7/assets/127780305/6228ed22-a83a-4d00-9acc-0f57a147b25a)


## Models
We explored various architectural configurations and hyperparameters. Our approach involved the creation of four distinct models, each with carefully modified attributes, aimed at enhancing our predictive power. 
We modified the quantity of layers, optimizer selection, activation function variations, and fine-tuning of neuron quantities and training epochs. These meticulous adjustments collectively contributed to the enhancement of our Credit Card Approval Prediction model's accuracy and reliability.
## Results
We achieved remarkable results. While the accuracy of all models was good, the highest accuracy we attained was 98%. This signifies that our predictive power in assessing credit card approval significantly improved through careful model architecture selection, hyperparameter tuning, and optimization.
## Conclusion
Our project not only seeks to develop an accurate predictive model but also aims to uncover hidden insights within these crucial dataset columns. By harnessing the power of data science, machine learning, and statistical analysis, we aspire to empower credit card companies with the tools they need to make informed and equitable lending decisions. 
