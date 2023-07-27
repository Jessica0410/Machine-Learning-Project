# K Means Cluster
K-Means Clustering is a simple unsupervised learning grouping the unlabeled dataset into different clusters. The goal of clustering is dividing the population or set of data points into a number of groups in order that the data points within each group contains mutual similar features. The number of groups depends on the decision of value of K.

### 1. K-means algorithm
K-Means algorithm compares the euclidean distance of the points to each  centroid and then groups them to the cluster whose centroid is nearest to the points. The points in same cluster have something similar according to the feature input. In other word, it assigns the data points to the cluster with minimal euclidean distance to the centroid means. Since data with some similar features are closer to each other.

### 2. K-means algorithm workflow
1. Randomly initialize k points. Those points are means or cluster centroids.
2. Categorize the data points to the nearest cluster by calculating the euclidean distance between data point and centroid. 
3. Recompute the centroid by calculating the means of all points within that cluster.
4. Repeat step 2 and 3 until the centroid remains the same.

### 3. K-means optimization
Goal: Minimize $J(c^{(1)},...,c^{(m)}, \mu_1,...,\mu_k)$ by keeping changing the cluster means and re-assigning the centorid  of each data point.

#### cost function

$$
J(c^{(1)},...,c^{(m)}, \mu_1,...,\mu_k) = \frac{1}{m}\sum_{i=1}^m||x^{(i)} - \mu_{c^{(i)}}||^2
$$


$c^{(i)}=$ index of cluster to which example $x^{(i)}$ is currenly assigned <br>
$\mu_k=$ cluster centroid $k$ <br>
$\mu_{c^{(i)}}=$ cluster centroid to which example $x^{(i)}$ has been assigned

#### cost function translation
Repeat{<br>
&nbsp;&nbsp;for $i=1$ to $m:$ <br>
    &nbsp;&nbsp;&nbsp;&nbsp; $c^{(i)}=$ index of nearest cluster centroid of $x^{(i)}$ ---- minimize $x^{(i)}-\mu_{c^{(i)}}$<br>
    &nbsp;&nbsp;for $k=1$ to $K:$<br>
    &nbsp;&nbsp;&nbsp;&nbsp; $\mu_k=$ avg of points in cluster $k$ ---- minimize $\mu_{c^{(i)}}$ <br> 
}

### K-means application
- **Image compression:** compress image from 256 to 16 gray levels - group all the pixels to 16 different clusters and pixels in same cluster are the same color.
- **Customer segmentation:** segment customers based on their purchase patterns,interestes or activities.

**This script implemented the K-Means algorithm from scratch** </br>
**Reference:**
[Cousera ML Specialization Unsupervised Learning](https://www.coursera.org/learn/unsupervised-learning-recommenders-reinforcement-learning)

