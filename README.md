# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: ENBANATHAN V
RegisterNumber:  212224220027

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
from sklearn import metrics # import metrics from sklearn
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

*/
```

## Output:
![Screenshot 2025-05-13 153226](https://github.com/user-attachments/assets/28176f83-44b3-4514-b81f-0e519a249ab7)
![Screenshot 2025-05-13 153236](https://github.com/user-attachments/assets/cabc68a2-7211-4338-a806-6c20ee25816f)
![Screenshot 2025-05-13 153248](https://github.com/user-attachments/assets/b5d33642-677f-4db6-b4db-35670b6f9ea7)
![Screenshot 2025-05-13 153305](https://github.com/user-attachments/assets/adc803e1-2446-4e74-8729-465c58c93c32)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
