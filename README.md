# SpeakX--Data-Science-Assignment
##### SRM-University---2024
## Problem Statement
Predicting Customer Churn in a Telecommunications Company
## Objective
---
The primary objective of this project is to develop a predictive model that can identify customers at risk of churning, enabling the company to take proactive measures to retain them

## Key Findings
---
1. The given Data set consists of 26.5% of customers who are churned.
2. The monthly charges are directly proportional to the Churn rate
3. The Total charges were inversely proportional to the Churn
4. HIGH Churn seen in case of  Month to month contracts, No online security, No Tech support, First year of subscription, and Fibre Optics Internet
5. LOW Churn is seen in case of Long-term contracts, Subscriptions without internet service and customers engaged for 5+ years
6. Factors like Gender, Availability of PhoneService have almost NO impact on Churn

## Approach 
---
### Data Preprocessing
Using pandas the data was preprocessed.This step identified the shape of the data,data types,the null values,and converted the numerical variables into categorical variables.

### Exploratory Data Analysis
For more accurate processing,
1. Cnverted the numeric "tenure" coulmn to categorical variable and dropped the coulmns that werent required further .
2. All the categorical variables were converted into dummy variables  for accurate modelling
3. Churn by monthly charges and total charges were visualised for insights.
Also identified that the data given is highly imbalanced as the churners are 26.5% and the number of non churners are 73.4%.

##### *To solve the imbalanced data problem , used SMOOT-ENN for upscaling of data in every model created*
#
### Feature Engineering
Identified that High churn was maximum in case of Month to month contracts, No online security, No Tech support, First year of subscription, and Fibre Optics Internet using the correlation matrix

### Model Building  
The model build using the given data set with *Upscaled data using SMOOT-ENN technique* were:

#### Decision Tree:

| Accuracy | Precision | Recall | F1 Score |
| ------------ | ------------ | ------------ | ------------ |
| 93.14 | 92.14 | 96.35 | 94.21 |

#### Random Forest:

| Accuracy | Precision | Recall | F1 Score |
| ------------ | ------------ | ------------ | ------------ |
| 92.77 | 90.97 | 96.24 | 93.53 |

#### XgBoost:

| Accuracy | Precision | Recall | F1 Score |
| ------------ | ------------ | ------------ | ------------ |
| 94.91 | 96.80 | 95.92 | 96.36 |

#### Logistic Regression:

| Accuracy | Precision | Recall | F1 Score |
| ------------ | ------------ | ------------ | ------------ |
| 97.85 | 98.70 | 97.28 | 97.98 |

### Model Evaluation
With the original data set , Random Forest and Logistic Regression have almost the same accuracy 
With the upscaled data, Logistics regression model provides the best accuracy of 97.85% on the testing data, which indicates that it is a very good predictor of churn.

### Result
According to our analysis, the most important factors related to churn are monthly charges, contract type, and internet service. Customers with high monthly charges and those with month-to-month contracts or no contracts are more likely to churn.

### Challenges :
- Handling the imbalanced data ,which was solved eventually with the SMOOT-ENN technique
- Understanding the ML models that can be used with the data as it contained both categorical variables and Numeric variables

### Conclusion
Our analysis recommends offering discounts to high monthly spenders and prioritizing retention efforts for customers with long contracts and high-speed internet. Leveraging a logistic regression model identifies at-risk customers, enabling targeted retention strategies.





