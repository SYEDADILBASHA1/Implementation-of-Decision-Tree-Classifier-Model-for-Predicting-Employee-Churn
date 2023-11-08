# EX-06 Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn
# DATE:12.10.2023

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Read the data frame using pandas.
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply decision tree Classifier on to the dataframe.
7. Get the values of accuracy and data prediction.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:  SYED ADIL BASHA
RegisterNumber:  212221043008

import pandas as pd
data=pd.read_csv("Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
## 1.Initial Data Set:
![ex 6 1](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/c6f6f883-d45e-4a5d-961e-bf41fb10e807)

## 2.data info:
![ex 6 2](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/3cac38b5-be41-45f6-a334-3b14ff8965f8)

## 3. Optimization of null values:
![ex 6 3](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/5bed4675-c083-442a-8280-877632912ab9)

## 4.Assignment of x and y values:
![ex 06 5](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/8e3a5f9b-06c6-4c59-a136-1f4da2fe50ea)

## 5.Converting string literals to numerical values using label encoder:
![ex 06 -6](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/76031f42-8c23-4ab8-945c-2f4fed323f5e)

## 6.Accuracy:
![Screenshot (2)](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/6efc2de3-3fcc-4a21-9313-5292d0118a37)


## 7.Prediction:
![ex 06 08](https://github.com/SYEDADILBASHA1/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/134796157/d3777dbf-6c84-4f19-8152-52206feb022e)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
