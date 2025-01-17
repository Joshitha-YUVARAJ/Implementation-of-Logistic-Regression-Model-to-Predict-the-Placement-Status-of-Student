# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages and print the present data.

2. Find the null and duplicate values.

3. Using logistic regression find the predicted values of accuracy , confusion matrices.

4. Display the results.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: YUVARAJ JOSHITHA
RegisterNumber: 212223240189

import pandas as pd
data=pd.read_csv("/content/Placement_Data.csv")
data.head()

data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)#Browses the specified row or column
data1.head()

data1.isnull().sum()

data1.duplicated().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"] )     
data1["status"]=le.fit_transform(data1["status"])       
data1 

x=data1.iloc[:,:-1]
x

y=data1["status"]
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy

from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
confusion

from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print(classification_report1)

lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])


 
*/
```

## Output:

## PLACEMENT DATA:
![Screenshot 2024-03-12 093713](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/fe1a8e27-2fa2-41e4-919e-099598e6e084)

## NULL DATA:
![Screenshot 2024-03-12 093938](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/6d6cc05d-5776-4aa5-a883-066aa60097fa)

## X DATA:
![Screenshot 2024-03-12 094455](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/83221a4e-174f-4c14-84de-4021b93fbf99)

## Y DATA:
![Screenshot 2024-03-12 094000](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/d1d6b679-391d-485e-ae7d-6f921affab10)

## Y PREDICTED:
![Screenshot 2024-03-12 094010](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/ed6c7c15-ce11-4b0b-a443-bcbd35feb136)

## ACCURACY:
![Screenshot 2024-03-12 094830](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/1a0a67ac-6058-435d-bd70-349b4e6ed0ea)

## CLASSIFICATION REPORT1:

![Screenshot 2024-03-12 094024](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/1a7c6373-1b9b-44d0-a81a-5f67ae4b679e)

## PREDICTION OF LR:
![Screenshot 2024-03-12 094052](https://github.com/Joshitha-YUVARAJ/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/145742770/d5fbfdb5-a837-4e1f-a143-f0ec937cc1f7)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
