# Develop By : Naveen Kumar.T
# RegisterNumber : 212223220067
# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2.Upload the csv file and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree inport DecisionTreeRegressor.
5.Import metrics and calculate the Mean squared error.
6.Apply metrics to the dataset, and predict the output.

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee
```
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
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

# Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)

## Initial Dataset:
![318789424-33faca45-0c8f-49fd-905d-954838a675ce](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/d4a8bb76-e36f-4122-a97a-96d62d7b63f5)

## Data Info:
![318789438-daed8dfd-55c0-4e58-bf3a-d62c3dfdffdd](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/1c7a5b70-5af5-47ce-962c-a0a347d81a57)

## Optimization of null values:

![318789457-005453a7-304b-48ee-8716-be3417e266c8](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/f32b9bd2-df7d-4750-8f72-6384a4433ddd)

## Converting string literals to numerical values using label encoder:
![318789472-49c1c499-bda8-47b6-b395-56bf36923a9d](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/cff95329-9914-4231-84e6-abf6c16a7a1d)

## Mean Squared Error:

![318789492-b36bf828-7382-4275-91d4-190ff0d2ed14](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/b0c6fdcb-0243-4403-8a43-8a97948084fa)

## R2 (Variance):
![318789505-6b239db9-34f5-4051-8c48-cbed92f83de9](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/7fb02a6c-c7ac-40ce-9dc2-193cba88e004)

## Perdicition:
![318789518-77e886b1-2968-4027-a2ce-6582665fa16a](https://github.com/820NaveenKumar208/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/154746066/1e712131-ec61-4379-accf-79fc6650a9c1)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
