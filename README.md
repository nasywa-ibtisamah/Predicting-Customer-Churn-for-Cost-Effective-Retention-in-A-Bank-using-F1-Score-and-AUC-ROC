# Project Description

Hello there :wave:
I hope this project finds you well!

In this project, I will predict whether the customers of Bank Beta is likely to leave the bank soon or not as the bank employees realize that it would be more cost-effective for the company to focus on retaining their loyal existing customers rather than attracting new ones.

I have data related to the past behavior of clients and their history of contract terminations with the bank.

**Objective**
To train a model with the highest possible F1 score with a minimum F1 score of 0.59 for the test dataset. Additionally, I will measure the AUC-ROC metric and compare it with the F1 score.

**Used Model**
1. Logistic Regression
2. Decision Tree
3. Random Forest

# Steps

1. Data Overview
2. Data Preprocessing
3. Splitting the Data
4. Assessing Model Quality
5. Normalizing the Features (Standard Scaler)
6. Improving Model's Quality
	- Hyperparamater Tuning
	- Upsampling
	- Downsampling
7. Testing Model on Test Dataset

## 1. Data Overview

**Data Description** 

**Features**
- `RowNumber` - index of string data
- `CustomerId` - customer ID
- `Surname` - last name
- `CreditScore` - credit score
- `Geography` - country of residence
- `Gender` - gender
- `Age` - Age
- `Tenure` - tenure of fixed-term deposit (in years)
- `Balance` - account balance
- `NumOfProducts` - number of bank products used by the customer
- `HasCrCard` - whether the customer has a credit card (1 - yes; 0 - no)
- `IsActiveMember` - level of customer's activity (1 - yes; 0 - no)
- `EstimatedSalary` - estimated salary

**Target**
- `Exited` - whether the customer has exited (1 - yes; 0 - no)

## 2. Pre-Processing Data

The following are data preprocessing steps I did in this project:
1. Standardize Column Names
2. Handling Missing Values
3. Drop Unused Columns
4. Categorizing Columns
5. Encode Features

## 3. Splitting the Data

The data will be splitted into:
1. Training Set: This data is used to train and build the model.
2. Validation Set: This data is used to optimize the model during its construction. It helps assess the model's ability to recognize patterns in a general sense. The validation set is also used to evaluate the accuracy of the created model. If the accuracy is not satisfactory, hyperparameter tuning can be performed.

3. Test Set: This data is used to test the model's performance.


## 4. Assessing Model Quality


1. Based on the performance results of the three models, the F1 scores from highest to lowest are as follows:

	- Random Forest model with an F1 score of 0.61 and an AUC-ROC score of 0.87

	- Decision Tree model with an F1 score of 0.47 and an AUC-ROC score of 0.67

	- Logistic Regression model with an F1 score of 0.11 and an AUC-ROC score of 0.67

2. The results of Random Forest passed the evaluation with a minimum F1 score of 0.59 for the validation set.

## 5. Normalizing the Features (Standard Scaler)

1. Based on the performance results of the three models after scaling, the F1 scores from highest to lowest are as follows:

	- Random Forest model with an F1 score of 0.61 and an AUC-ROC score of 0.87

	- Decision Tree model with an F1 score of 0.50 and an AUC-ROC score of 0.69

	- Logistic Regression model with an F1 score of 0.35 and an AUC-ROC score of 0.79

2. The results of Random Forest passed the evaluation with a minimum F1 score of 0.59 for the validation set.

4. When compared to the results before scaling, the Random Forest performance remained unchanged. Meanwhile, Logistic Regression improved by more than 3 times from 0.11 to 0.35, and Decision Treee increased by 0.03 for the F1 score and decreased by 0.02 for the AUC-ROC.

## 6. Improving Model's Quality


### Conclusion of Improving Model's Quality Step <a 

From the three processes (class_weight adjustment, upsampling, downsampling), the best F1 score is achieved by:

- Model: Random Forest

- Method: hyperparameter tuning (class weight adjustment)

- Depth: 10

- n_estimators: 100

## 7. Testing Model on Test Dataset

The result:
- F1 score = 0.5915966386554622 
- AUC-ROC score = 0.8517582158570531

# General Conclusion

The F1_score on the test dataset is 0.59, which meets the minimum requirement, and the AUC-ROC score is 0.85.

Therefore, I would recommend Bank Beta to use the Random Forest model with a depth of 10 and n_estimators of 100 to predict whether a customer is likely to leave the bank or not.
