# Supervised Machine Learning Homework - Predicting Credit Risk

In this assignment, I built a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

I used this data to create machine learning models to classify the risk level of given loans. Specifically, I compared the Logistic Regression model and Random Forest Classifier.

### Retrieve the data

I used an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

* `2019loans.csv`
* `2020Q1loans.csv`

## Preprocessing: Convert categorical data to numeric

To convert the categorical data to numeric columns, I created a training set from the 2019 loans using pd.get_dummies(). I also created a testing set from the 2020 loans, also using pd.get_dummies(). The data structures were slightly different, so I used code in Jupyter Notebooks to make the dataframes similar so that the prediction model would work on both datasets.

## Consider the models

Looking at the datasets, I believe that the logistic regression model will perform better for this dataset. With over 80 variables to consider, the Logistic model will win out over the Random Forest model. Based on my research, Random Forest is recommended for simple classification problems.

## Fit a LogisticRegression model and RandomForestClassifier model

My prediction was wrong seeing as the random forest classifier model is the most acurate without scaling the models.

## Revisit the Preprocessing: Scale the data

The logistic regression became the better classifier after scaling. It had an accuracy score of .66.
The Random Forest model decreased in accuracy from .64 to .5. I would be hesitant about implimenting this for credit rating purposes. There is still far too much inaccuracy. I am sure money would be lost on a consistent basis if loan decisions were based on this model.

### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)

- - -

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
