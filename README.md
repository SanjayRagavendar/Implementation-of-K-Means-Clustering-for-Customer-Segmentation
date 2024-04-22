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
## Output:
![K Means Clustering for Customer Segmentation](sam.png)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
