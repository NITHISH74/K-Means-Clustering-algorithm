# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
Import pandas,mathplotlib.pyplot,sklearn,seaborn,warnings.


### Step2
Read the csv fileusing df.head() and assign it to the variables



### Step3
Plot the group using scatterplot.


### Step4
Find the centroid using KMeans from sklearn module.


### Step5
Run the program and display the graph.



## Program:
```
# NAME: NITHISHWAR
# REF NO: 21002766

import pandas as pd
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
import seaborn as sns
x1=pd.read_csv('clustering.csv')
print(x1.head(2))
x2=x1.loc[:,['ApplicantIncome','LoanAmount']]
print(x2.head(2))

x=x2.values
#print(x)
sns.scatterplot(x[:,0],x[:,1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmeans=KMeans(n_clusters=4)
kmeans.fit(x)
print("Cluster centers:",kmeans.cluster_centers_)
print("Labels:",kmeans.labels_)
predict_class = kmeans.predict([[9000,1200]])
print("Cluster group for application income 9000 and loanamount 120 is",predict_class)

```

## Output:

![image](https://user-images.githubusercontent.com/94164665/154079504-4f2227e7-41c2-44b2-b0bb-b284fc64db28.png)


## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.
