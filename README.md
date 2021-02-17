# Titanic
Using Machine Learning algorithm to predict if someone survived the Titanic shipwreck. 

# Project Overview

- Two sets of data (i.e. Train and Test set) concatenated and preprocessed before modeling 
- Removed outliers, imputed any missing values and normalized the fare to obtain more accurate predictions.
- Engineered Features such as Family Size, Title (i.e 'Fam_Size', 'Title').
- Optimized and classified using Logistic Regression, K Neighbors Classifier, Support Vector Classifier, Gaussian Naive Bayes, Decision Tree Classifier, Random Forest Regressor.
- Voting Classifier is also used which takes all of the inputs and averages the results.
- Plot results using Bar graph of the Survivability of the passengers on the test data based on the trained.
- Accurately predicted 77.9% of the test set.

# Reference

**Python Version:** 3.8</br>
**Packages:** numpy, pandas, seaborn, matplotlib</br>
**Titanic Dataset:** [Titanic: Machine Learning from Disaster](https://www.kaggle.com/azeembootwala/titanic?select=test_data.csv)</br>


# Data Preprocessing

- Drop null values from Embarked (only 2)

- Include only relevant variables (Since we have limited data, I wanted to exclude things like name and passanger ID so that we could have a reasonable number of features for our models to deal with)
  -Variables: 'Pclass', 'Sex','Age', 'SibSp', 'Parch', 'Fare', 'Embarked'

- Do categorical transforms on all data. Usually we would use a transformer, but with this approach we can ensure that our traning and test data have the same colums. We also may be able to infer something about the shape of the test data through this method. (use onehot encoder from sklearn library).

- Impute data with median for fare and age 

- Scaled data 0-1 with standard scaler


# Exploratory Data Analysis

Light Data Exploration

1) For numeric data
  - Made histograms to understand distributions
  - Pivot table comparing survival rate across numeric variables


2) For Categorical Data
  - Made bar charts to understand balance of classes
  - Made pivot tables to understand relationship with survival

![](https://github.com/roywong96/Titanic/blob/main/images/corrplot.png)


# Model Building and Performance

- Before going further, I like to see how various different models perform with default parameters. 
- Function written for many machine learning models and return its accuracy.
![](https://github.com/roywong96/Titanic/blob/main/Data/TitanicAcc.png)

# Results

- Results of the survivability is filled in the test dataset using the trained model 
- Decision Tree Classifier is chosen as it has the highest accuracy.

![](https://github.com/roywong96/Titanic/blob/main/images/Survival.png)

