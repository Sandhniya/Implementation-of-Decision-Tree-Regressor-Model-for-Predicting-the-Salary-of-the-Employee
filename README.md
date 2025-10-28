# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Import the standard libraries.

Upload the dataset and check for any null values using .isnull() function.

Import LabelEncoder and encode the dataset.

Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

Predict the values of arrays.

Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

Predict the values of array.

Apply to new unknown values.


## Program:
```


import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position", "Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse
r2 = metrics.r2_score(y_test, y_pred)
r2
dt.predict([[5,6]])
```

 Output:sa
<img width="730" height="656" alt="image" src="https://github.com/user-attachments/assets/3760b536-94c9-4894-8839-cd524026779f" />

<img width="814" height="611" alt="image" src="https://github.com/user-attachments/assets/4a5d28bd-3bf2-43a9-a2cd-9e251a3741ac" />

<img width="429" height="556" alt="image" src="https://github.com/user-attachments/assets/5ce771e1-2894-4ee7-b069-8c9d72a3e1b0" />

<img width="1165" height="818" alt="image" src="https://github.com/user-attachments/assets/221f06ea-a8fd-46d4-a89f-09c8e84014e9" />

<img width="1449" height="105" alt="image" src="https://github.com/user-attachments/assets/4bebd4b6-dac6-48e1-87f8-5d1dbd9b8366" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
