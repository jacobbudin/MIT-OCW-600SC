# Introduction to Computer Science and Programming
## Lecture 21

### K-means clustering
K-means clustering requires asking for *n* number of clusters, rather than seeing the grouping occur iteratively with each successive grouping. Initial centroids are chosen at random. Clusters are initially empty, and the inital centroids are added. For each cluster, create new clusters and determine the distance between the cluster's centroid and new potential entrant to the cluster. This is done repetitively. At the end, the *coherence* is determined, the maximum distance of the cluster with points most distant from one another.

Since initial centroids are chosen at random, results will be different each time. Use *mix-max metric* to select the clustering that is the best.

### Clustering counties
Filters have been added the nullify certain characteristics. Attributes' values have been normalized so numerically large attributes (e.g., population) do not receive greater weight in calculations.

If clustering is done at random, the clusters' mean values will gravitate towards the global mean (creating a flat graph, or if intervals are large, one big spike). Regenerating the graph based on gender ratio creates a *bimodal graph* (spikes on the two ends, low in middle).

### Supervised vs. unsupervised learning
In *supervised learning*, there is a training set with labels, in which one infers a relationship between features and labels. In *unsupervised learning*, the training set is unlabeled data, in which one infer relationships among points. These techniques are similar to *regression*, fitting curves to data, and the same concern exists: be wary of overfitting, especially on small data sets. Also: Features matter; which you choose, whether they're normalized, if and how much they're weighted. Domain knowledge is important in choosing features.

### Graph theory
If given a graph of airplane flights and a source and destination, what's the quickest, cheapest, least hops, way of travelling from point A to point B? These questions are answered by graphs. A *graph* is a set of nodes (vertices) connected by a set of edges (arcs). If the edges are unidirectional, the graph is a *digraph*.

Euler, a resident of Prussia, tried to determine if bridges could be crossed only once in traversing a city. He simplified the problem: You couldn't touch a point with returning; therefore you need an even number of edges to do so.

You can extend this theory by giving edges weights (e.g., the toll on a road), creating a weighted graph.

Graphs can be represented in Python with simple classes (Node, Edge, Graph, Diagraph). Results can be representated as adjaceny matrix (for many connections) or adjacency list (for few connections).