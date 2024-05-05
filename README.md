# EX-06 Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
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
```
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: PRADEEP V 
RegisterNumber: 212223240119
*/
```



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

## Output:
# head()
![320197629-5e01e860-7b5f-4cc7-9ef7-85dc42ae12b4](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/da220949-9cd7-4c10-8360-928c971a93a0)
# info()
![320197660-6c5cec2d-9217-4476-9b5f-b7952fdbc45a](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/cc04b026-b0c3-4241-b076-c10c736e186d)
# isnull().sum()
![320197708-06439654-7ed0-4631-846a-465bde883f6e](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/f30d2751-d37e-474e-ad95-f50107a62c2e)
# value count
![320198015-3b0430a4-8b3d-4543-a7df-d61bb45af776](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/1a15f492-4f2d-4a60-937e-384c6fca3eeb)
# head after transform
![320198055-22a2ace5-bae1-4269-aef0-ff5ea36d6e2e](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/2cc07f8f-4c39-426d-a9e3-4a3af15e8752)
# x.head()
![320198064-9db305ef-438a-4744-a2ea-e91672e2e44f](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/921df967-735b-49cd-82b0-a3fe042bb346)
# accuracy
![320198107-c0941cd7-26be-4727-aa30-b8bd723383ab](https://github.com/velupradeep/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/150329341/aca67da6-610d-413a-ae28-c3ab4716736d)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
