# Titanic
Using Machine Learning algorithm to predict if someone survived the Titanic shipwreck. 


# Data Preparation

- Data Obtained From: https://www.kaggle.com/azeembootwala/titanic?select=test_data.csv

# 1) Understand the shape of the data (Histograms, box plots, etc.)

- Using '.info()', '.describe()', '.shape()'
  - to explore the features in the data
  - look at the descriptive statistics of the data
  - checking the dimensions of the data
- Histograms and boxplots 
- Value counts 

# 2) Data Exploration

Light Data Exploration

1) For numeric data
  - Made histograms to understand distributions
  - Pivot table comparing survival rate across numeric variables


2) For Categorical Data
  - Made bar charts to understand balance of classes
  - Made pivot tables to understand relationship with survival

# 3) Data Preprocessing for Model

- Drop null values from Embarked (only 2)

- Include only relevant variables (Since we have limited data, I wanted to exclude things like name and passanger ID so that we could have a reasonable number of features for our models to deal with)
  -Variables: 'Pclass', 'Sex','Age', 'SibSp', 'Parch', 'Fare', 'Embarked'

- Do categorical transforms on all data. Usually we would use a transformer, but with this approach we can ensure that our traning and test data have the same colums. We also may be able to infer something about the shape of the test data through this method. (use onehot encoder from sklearn library).

- Impute data with median for fare and age 

- Scaled data 0-1 with standard scaler

# 4) Basic Model Building

- Before going further, I like to see how various different models perform with default parameters. 
- Function written for many machine learning models and return its accuracy.
![](https://github.com/roywong96/Titanic/blob/main/Data/TitanicAcc.png)

# 5) Results

- Results of the survivability is filled in the test dataset using the trained model 
- Decision Tree Classifier is chosen as it has the highest accuracy.
