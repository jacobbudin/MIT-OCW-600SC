# Introduction to Computer Science and Programming
## Lecture 19

### Knapsack problem (continued)
*Greedy algorithms* solved the problem, but didn't necessarily select the optimal solution. *Brute force algorithms* guarantee an optimal solution, but depending on input size, takes too long to run.

Brute force approach: Generate binary numbers of all possibilities (whether to take an item or not), then record the max in the buffer and check against constraint for each possibility. Results in the best subset of items, unlike previous greedy algorithms. Why better? Greedy algorithms chose locally optimal values which does not guaranetee a global optimal. The complexity of this problem is *inherently exponential*. (There are techniques for [usually] speeding this up, that we'll learn later.)

### Machine learning
> Machine learning, a branch of artificial intelligence, is about the construction and study of systems that can learn from data. For example, a machine learning system could be trained on email messages to learn to distinguish between spam and non-spam messages. After learning, it can then be used to classify new email messages into spam and non-spam folders.

*Machine learning* means building programs that learn via *inductive inference*: building a model  based an observation about a phenomena that can then predict the future. There are two approaches to machine learning:

1. *Supervised learning*: Associate a label with each example in a training set. If the label is discrete, it's a *classification problem* (e.g., a credit card transaction is associated with owner or it is not). If the label is a real value, it's a *regression problem*.
2. *Unsupervised learning*: Determining regularities in the data; to discover the structure upon which you can predict. (e.g., finding the cluster in a set of graphed data)

In example, learning the color of points based on `<x,y>` coordinates. Questions to ask before attempting to implement learning techniques: Are the labels accurate? Is past representative of the future? Do you have enough training data to generalize? What features should be extracted? How tight should the fit be? In example, there are two possible classifications: by `x` value (some training error, one point) or in triangle/angle/vector area (no training error). Triangle isn't necessarily better—just like overfitting with curve.

Clustering is used in many industries (e.g., marketing). It can be focused/divided by certain metrics. Netflix, Amazon.com, Wal-Mart use clustering to make recommendations, classify people, etc.

What properities should clustering have? 1. Low intra-cluster dissimilarity—all the points in the same cluster should be similar. 2. High inter-cluster dissimiliarity—points in different clusters should be different from one another.

We measure cluster quality with `variance(c) = sum of (mean(c) - x)^2` to express cohesion or lack thereof. Minimize variance? No, because you could have clusters of unit one. We need a *constraint* (e.g., the maximum number of clusters, maximum distance between clusters).

Clustering is also computationally expensive: People usually resort to *greedy algorithms*. 1) *K-means clustering*: I want "K" clusters (not guaranteed to find best). 2) *Hierarchical clustering*.

#### Hierarchical clustering
For example, a NxN matrix of distance between cities:

			BOS	NY	CHI	...
	BOS 	0	206	
	NY			0
	...

**Steps:**

1. Assign each item to its own cluster.
2. Find the most similar pair of clusters and merge them. (in this case, merge NY and BOS)
3. Continue process until all items are in one cluster (cut it off whenever).

This is *agglomerative clustering*, because we're combining them. Step 2 is problematic; we need a *linkage criteria*: 1) single-linkage (best case, shortest distance between any pair), 2) complete linkage (the opposite, worst case: distance between the points furthest from each other), 3) average (take all distances).

Example in action:

	BOS		NY	CHI	DEN	SF	SEA
	[BOS,NY]	CHI	DEN	SF	SEA
	[BOS,NY,CHI]	DEN SF 	SEA
	[BOS,NY,CHI]	DEN [SF,SEA]
	# Depending on linkage:
	[BOS,NY,CHI]  	[SF,SEA,DEN]
	# Or:
	[BOS,NY,CHI,DEN][SF,SEA]
	[BOS,NY,CHI,DEN,SF,SEA]
	
This technique is used often. Weakness: complexity is a minimum O(n^2); not necessarily the optimal clustering. Also: More complexity is common (what about bus and train routes?). *Feature vectors* are frequently used (e.g., defining cities like: `<gps, population>`).