# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.


## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: Divyashree B S
RegisterNumber:  212221040044

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

print("data.head():")
data.head()

print("data.info():")
data.info()

print("isnull() and sum():")
data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
print("data.head() for salary:")
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
print("MSE value:")
mse

r2=metrics.r2_score(y_test,y_pred)
print("r2 value:")
r2

print("data prediction:")
dt.predict([[5,6]])
```

## Output:


<img width="200" alt="ex7 op1" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/25035939-8508-4cc6-9096-29c4a4896cc4\n">

<img width="320" alt="ex7 op2" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/a86887c6-1040-4016-ae69-9fc073ac8b91\n">

<img width="177" alt="ex7 op3" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/dad67506-8cf2-49f6-ab0b-9378782be680">\n

<img width="168" alt="ex7 op4" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/1b2df097-22de-40c0-a0fa-f85c474b7d77">\n

<img width="527" alt="ex7 op5" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/d44c1e91-ae24-4b7c-99df-3cc3504f22de">\n

<img width="450" alt="ex7 op6" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/582ca0a9-0eb9-42bf-a210-929f8f57adbf">\n

<img width="881" alt="ex7 op7" src="https://github.com/divvisha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/127508123/c08d74d6-615e-4996-89bb-27db7a46ae23">


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
