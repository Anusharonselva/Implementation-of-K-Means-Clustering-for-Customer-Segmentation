# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Print the outputs and end the program
 
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: S.ANUSHARON
RegisterNumber:  212222240010
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1) (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
  kmeans = KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
  
  plt.plot(range(1,11),wcss)
plt.xlabel("No. of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

Km = KMeans(n_clusters = 5)
Km.fit(data.iloc[:,3:])

y_pred=Km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segmets")
*/
```

## Output:

Data.head():

![Screenshot (307)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/32438e0f-4295-4c63-8d83-dbc1d11c77f4)

Data.info():

![Screenshot (308)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/a10bfe40-402c-478b-9480-d1623d3049e1)

Data.isnull.sum() function:

![Screenshot (309)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/9ac4bf58-a52b-4977-a25c-504db9e4bcf2)

Elbow Method Graph:

![Screenshot (310)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/5e7e2a8d-2c36-4cd1-90b7-60ef15ab2450)

KMeans clusters:

![Screenshot (311)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/b4bace53-ba71-4672-b6c6-f5bb91bce3ce)

Customer Segments Graph:

![Screenshot (312)](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/835d7a15-3dc1-4ab0-bd39-62e0113ee5f7)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
