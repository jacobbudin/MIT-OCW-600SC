# Introduction to Computer Science and Programming
## Lecture 20

### Clustering (continued)
A *feature vector* allows clustering by multiple parameters ("features"). Problem: Comparing items when units are incomparable (e.g., miles distance vs. degrees Farenheit temperature)—and even when they are (e.g., height in inches vs. weight in inches) due to level of variance. The moral: Think hard about how to scale features, because will have a dramatic influence on your clustering.

Feature selection and scaling is critical. It is done using *domain knowledge*. One technique is the *Minkowski Metric*:

	dist(X1, X2, p) = sum(abs(X1-X2)^p)^(1/p)

Set `p = 2` for Euclidean distance ("as the bird flies").  Set `p = 1` for Manhattan distance (using street grid, not "as the bird flies"). *Nominal categories* include categories like colors (blue vs. green). They need to be converted to numbers (doing so is an example of domain knowledge). Scaling these values is callled *normalization*, typically values between zero and one.

#### Clustering Mammals
Features and weighting mammals would have enormous effect on clustering. How to choose? You choose. For example, use dental records for each mammal to determine the clustering for what they eat.

In this case, each point is a mammal. Here, the clustering [to two clusters] is poor, because there's no normalization of different types of teeth. If one type of tooth has a greater dynamic range, it can skew clustering. In this case, scaling by `1/max` to get values between zero and one for same dynamic range. Changing this range produces improved results.

### Clustering Counties
Larger, or more complicated feature vectors cannot be computed by the previous algorithm due to its complexity. (There are 3,100 counties in the United States. The first step in clustering needs to compare `3,100^2`.) A clustering of New England countries prints Middlesex as first cluster, since it has a large population and had no scaling. With scaling on (`1/max`), a very different cluster.

### More efficient clustering
*K-means clustering* is much faster—near linear.

1. Choose `K`: the number of clusters you want when done.
2. Choose `K` points as initial centroids (usually chosen at random)
3. Assign points to the nearest centroid
4. For each of `K` clusters, choose a new centroid
5. Assign each point to nearest centroid
6. Repeat steps 4 and 5 until the change is small