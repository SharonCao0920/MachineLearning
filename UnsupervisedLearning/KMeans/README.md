# Python for K-Means
[Detail](https://github.com/SharonCao0920/MachineLearning/blob/main/UnsupervisedLearning/KMeans/Kmeans.ipynb)

### Data

```
import matplotlib.pyplot as plt

x = [1.5,1,2,5,3.5,4.5,2.5]
y = [1,2,3.5,6,4.,5,4.5]

plt.scatter(x, y)
plt.show()
```
### Analysis

```
from sklearn.cluster import KMeans

data = list(zip(x, y))
inertias = []

for i in range(1,len(x)+1):
    kmeans = KMeans(n_clusters=i)
    kmeans.fit(data)
    inertias.append(kmeans.inertia_)

plt.plot(range(1,len(x)+1), inertias, marker='o')
plt.title('Elbow method')
plt.xlabel('Number of clusters')
plt.ylabel('Inertia')
plt.show()
```
### Results
```
kmeans = KMeans(n_clusters=2)
kmeans.fit(data)

plt.scatter(x, y, c=kmeans.labels_)
plt.show()
```
