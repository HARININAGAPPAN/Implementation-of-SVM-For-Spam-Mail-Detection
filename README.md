# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Detect File Encoding: Use chardet to determine the dataset's encoding.

2.Load Data: Read the dataset with pandas.read_csv using the detected encoding.

3.Inspect Data: Check dataset structure with .info() and missing values with .isnull().sum().

4.Split Data: Extract text (x) and labels (y) and split into training and test sets using train_test_split.

5.Convert Text to Numerical Data: Use CountVectorizer to transform text into a sparse matrix.

6.Train SVM Model: Fit an SVC model on the training data.

7.Predict Labels: Predict test labels using the trained SVM model.

8.Evaluate Model: Calculate and display accuracy with metrics.accuracy_scor

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Harini N
RegisterNumber: 212223040057
import chardet
file='spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect (rawdata.read(100000))
result
import pandas as pd
data=pd.read_csv('spam.csv', encoding='Windows-1252')

## Output:
![SVM For Spam Mail Detection](sam.png)
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train, x_test, y_train,y_test=train_test_split(x,y,test_size=0.2, random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train, y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
<img width="708" height="150" alt="image" src="https://github.com/user-attachments/assets/cfd73d13-a5d0-4dbb-b001-0d7cf07166ad" />

<img width="726" height="237" alt="image" src="https://github.com/user-attachments/assets/7ea1649c-5963-4b43-8e91-df6b73d888ee" />

<img width="414" height="274" alt="image" src="https://github.com/user-attachments/assets/b7717939-a2e7-47eb-8d2a-91c1d218bd09" />

<img width="220" height="169" alt="image" src="https://github.com/user-attachments/assets/53b47314-2dd2-4673-96a1-b982959f099e" />

<img width="653" height="184" alt="image" src="https://github.com/user-attachments/assets/cc07bfc6-e6c2-423d-bf7a-5000482deeb8" />

<img width="422" height="131" alt="image" src="https://github.com/user-attachments/assets/d50988b6-7405-4c84-84f2-256d07ba17bf" />







## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
