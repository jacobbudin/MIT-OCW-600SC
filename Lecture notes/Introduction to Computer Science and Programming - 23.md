# Introduction to Computer Science and Programming
## Lecture 23

### Dynamic programming (continued)
Two properties need to exist in order to employ dynamic programming: 1) optimal substructure (can combine a globally optimal solution by combining locally optimal solutions, e.g., merge sort) , and 2) overlapping subproblems (solving a subproblem more than once,e.g., using memoization [performing a table look-up]).

Back to shortest path problem: if the fastest path from A to C is A - B - D - E - C, then the fastest path from B to E must be through D. Dynamic programming can also be used in the zero-one* knapsack problem. (Must "take" [steal] an item or leave it; cannot take part of an item.) Implement a decision tree to determine optimal solution (i.e., consider taking or not taking each item). It can use dynamic programming; the subproblem is: given a set of items and an the available weight, which items should we take. Use Python dictionaries (hash tables) to determine whether a value is stored; if not, compute and store in dictionary.

Be careful of: function argument with mutable type defaults and recursive stack limits.

Improvements in speed with memoization depends on the items to consider and the available weight. More items increases times. Greater "space"/weight capacity to fill increases time. There are no miracles: if all items vary in weight, "overlapping subproblem" criteria is not met and memoization is nullified. 