# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas module and import the required data set.
2. Find the null values and count them.
3. Count number of left values.
4. From sklearn import LabelEncoder to convert string values to numerical values.
5. From sklearn.model_selection import train_test_split.
6. Assign the train dataset and test dataset.
7. From sklearn.tree import DecisionTreeClassifier.
8. Use criteria as entropy.
9. From sklearn import metrics.
10. Find the accuracy of our model and predict the require values.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: SURIYA RAJ K
RegisterNumber: 212223040216
import pandas as pd
data=pd.read_csv("Employee (1).csv")
data.head()
data.info()
```

![image](https://github.com/user-attachments/assets/8ee57395-36a4-43cd-bc22-8a134c10ae93)
```

from sklearn. preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
```
![image](https://github.com/user-attachments/assets/c05f29d0-6d12-4e6b-861b-b1ab3d24ed0f)

```

x=data[["satisfaction_level","last_evaluation", "number_project", "average_montly_hours","time_spend_company", 
        "Work_accident", "promotion_last_5years", "salary"]]
x.head()
y=data["left"]
x.head()
```
![image](https://github.com/user-attachments/assets/62a44b69-f0ca-4ac8-8f47-35a273e225f5)





```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier (criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn.metrics import accuracy_score
accuracy=accuracy_score (y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

![image](https://github.com/user-attachments/assets/9c543820-a2c4-4b2d-9eb4-ce2c3831aacd)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
