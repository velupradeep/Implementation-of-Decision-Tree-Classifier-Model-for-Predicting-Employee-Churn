                                                               #NAME:PRADEEP V
                                                               #REG NO:212223240119

# EX-06 Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import pandas module and import the required data set.
2.Find the null values and count them.
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.
## Program:
```
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/Employee .csv")
data.head()
data.info()
data.isnull().sum()
data['left'].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data.head()
x=data[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
y=data['left']
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_predict)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PRADEEP V 
RegisterNumber: 212223240119
*/
```

## Output:
![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/440ddbfa-e582-4be4-bb71-42ea5430edfd)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/a4119997-94cc-4085-8db5-bfac7483c935)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/b007dc9a-d581-44ef-8e90-37a7e39f7a05)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/2728883f-f326-4eb4-8618-4e07a5674b28)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/a05fbee0-6359-462a-b131-70b0a11e47a5)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/a93325cf-e050-408f-a0ac-280f402e6817)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/dc49799c-de80-44d2-a796-a3d38ae07cc8)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/7547afb6-b10b-4685-89dc-c9077b137561)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/2e46dc5a-4307-49c5-b220-c03e6495fd03)

![image](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/8ea21779-b19e-410d-a5e3-19ca07700ec1)
















## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
