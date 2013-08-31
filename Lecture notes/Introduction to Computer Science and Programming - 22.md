# Introduction to Computer Science and Programming
## Lecture 22

### Graphs (continued)
Common problems with graphs include determining: the shortest path, the shortest weighted path (e.g., Google Maps, which minimizes time, not distance), the cliques (a set of nodes such that there exists a path connecting each node in the set), the minimum cuts (given two sets of nodes find the minimum number of edges that if cut would be disconnected; important in, for instance, power line distribution).

Visualizing graphs can be useful in determining the source of an outbreak of tuberculosis. Whereas shortest path can be used to track relationships on a social networking site. As presented, this algorithm is a recursive depth-first search (DFS). The base case is when you already exist on the node that is your destination. The recursive case begins by choosing children until it A) reaches a node with no children, B) reaches the destination, or C) reaches a previously-reached node.

Use a function argument to track previously-visited nodes. Unfortunately, there are redundancies in look-ups. *Memoization* is the practice of storing the solutions to previously-solved problems to speed up problems, a subset of *dynamic programming*. You can perform dynamic programming on problems that fill two criteria: 1) optimal substructure (you can determine the globally optimal solution by combining locally optimal solutions) and 2) overlapping subproblems (benefits from successive problems of the same arguments).