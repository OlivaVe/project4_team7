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

In order for us to be able to work with this dataset, we had to do some modifications as part of an ETL process. 
1. We had the data split into 2 documents, so first we had to merge them together and create a new DataFrame.
## Models
We explored various architectural configurations and hyperparameters. Our approach involved the creation of four distinct models, each with carefully modified attributes, aimed at enhancing our predictive power. 
We modified the quantity of layers, optimizer selection, activation function variations, and fine-tuning of neuron quantities and training epochs. These meticulous adjustments collectively contributed to the enhancement of our Credit Card Approval Prediction model's accuracy and reliability.
## Results
We achieved remarkable results. While the accuracy of all models was good, the highest accuracy we attained was 98%. This signifies that our predictive power in assessing credit card approval significantly improved through careful model architecture selection, hyperparameter tuning, and optimization.
## Conclusion
Our project not only seeks to develop an accurate predictive model but also aims to uncover hidden insights within these crucial dataset columns. By harnessing the power of data science, machine learning, and statistical analysis, we aspire to empower credit card companies with the tools they need to make informed and equitable lending decisions. 
