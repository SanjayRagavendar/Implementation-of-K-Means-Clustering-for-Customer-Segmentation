# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```py
# Program to implement the K Means Clustering for Customer Segmentation.
# Developed by: Sanjay Ragavendar  
# RegisterNumber:  212222100045
```
```py
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv('/content/Mall_Customers.csv')
```
```py
data.head()
```
```py
data.info()
```
```py
data.isnull().sum()
```
```py
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans= KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
```
```py
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
```
```py
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
```
```py
y_pred=km.predict(data.iloc[:,3:])
y_pred
```
```py
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"], df0["Spending Score (1-100)"],c="red", label="cluster0")
plt.scatter(df1["Annual Income (k$)"], df1 ["Spending Score (1-100)"],c="black", label="cluster1")
plt.scatter(df2["Annual Income (k$)"], df2 ["Spending Score (1-100)"],c="blue", label="cluster2")
plt.scatter(df3["Annual Income (k$)"], df3["Spending Score (1-100)"],c="green", label="cluster3")
plt.scatter(df4["Annual Income (k$)"], df4["Spending Score (1-100)"],c="magenta", label="cluster4")
plt.legend()
plt.title("Customer Segments")
```
## Output:
### data.head()
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/a90e283e-4e44-4d42-8053-3c7d01e45233)


### data.info()
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/499cb037-b637-4bf6-9598-06a470daec51)


### data.isnull().sum()
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/54d5f8c9-df53-4090-9bdf-b29b142fbf87)

### plot
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/891c503c-7168-4a90-a90b-1da0eafbfc15)

### y_pred
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/26f160fa-3f8b-4077-b808-b37b306010a0)

### k_means clustering
![image](https://github.com/SanjayRagavendar/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/91368803/c4eb1322-db44-42e7-90e9-880b7e24c738)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
