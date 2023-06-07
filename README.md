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
![K Means Clustering for Customer Segmentation](sam.png)
![13 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/a1281767-bb24-484c-9ec6-c3b13d9496b3)

![14 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/5e1f9047-344b-49b6-870e-2731cd642e5d)

![15 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/e3bd352c-cd0a-4ac3-a8e9-7602de28049f)

![17 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/6f047290-e9a4-47df-93b9-4ada3e9046d5)

![18 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/3ae17c50-515c-417f-9bf9-8f7264951d69)

![19 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/a9829904-d067-4799-9a41-437ff45069c6)

![19 2](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/594a9ea7-a41a-456f-8326-a0e041e96228)

![46 1](https://github.com/Anusharonselva/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405600/70203c1c-6aa9-415e-915a-445e071b6bfd)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
