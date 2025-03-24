import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.datasets import load_iris
iris = load_iris()
data = pd.DataFrame(iris.data, columns=iris.feature_names)
kmeans = KMeans(n_clusters=3, random_state=42, n_init=10).fit(data)
print(pd.crosstab(iris.target, kmeans.labels_, rownames=['True Species'],
colnames=['Cluster']))
plt.scatter(data['sepal length (cm)'], data['sepal width (cm)'], c=kmeans.labels_,
cmap='viridis', s=50)
centroids = kmeans.cluster_centers_
plt.scatter(centroids[:, 0], centroids[:, 1], c='red', marker='x', s=200,
label='Centroids')
plt.xlabel('Sepal Length (cm)')
plt.ylabel('Sepal Width (cm)')
plt.title('K-Means Clustering')
plt.legend()
plt.show()

