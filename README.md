# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
~~~
1.Import the necessary packages using import statement. 
2.Read the given csv file and print the number of contents to be displayed. 
3.Split the dataset using train_test_split. 
4.Calculate Y_Pred and accuracy. 
5.Display the result.
~~~
## Program:
```
/*

Program to implement the SVM For Spam Mail Detection..
Developed by: VETRIVEL S
RegisterNumber:  212221240060


import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["EmailText"].values
y=data["Label"].values
from sklearn.model_selection import train_test_split 
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
  
*/
```

## Output:
![SVM For Spam Mail Detection](sam.png)

### data.head()
![1](https://user-images.githubusercontent.com/95363138/174320744-ebacec80-e4bf-4cb5-a417-46ff092c24bb.png)

### data.info()
![2](https://user-images.githubusercontent.com/95363138/174320764-82c55d1c-e06f-4905-ba66-f55517c1a332.png)

### Data.isnull().sum()
![3](https://user-images.githubusercontent.com/95363138/174320772-8fba71ab-2332-4e0d-9632-9881a622499a.png)

### y_pred
![4](https://user-images.githubusercontent.com/95363138/174320792-6ce5a00c-aaa2-41ec-a41e-f06ba5e60972.png)

### accuracy
![5](https://user-images.githubusercontent.com/95363138/174320816-40f3197c-d14d-4027-a931-43aa4c8464cc.png)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
