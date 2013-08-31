# Introduction to Computer Science and Programming
## Lecture 18

### Coefficient of determination (R^2)
R^2 of 1 is perfect. R^2 of 0 is useless (no predicative power). For instance, in case of trajectory of percentile, a linear fit has an r^2 of 0.0177 whereas a quadratic fit has an r^2 of 0.98. (The other 2% is experimental error.) The quadratic model is good.

### Making determinations on models
How much time does it take to fall? Peak of parabola occurs midway through launch and target. Time is a function of acceleration due to gravity.

1. Start with an experiment to gather data (in this case, about the behavior of a physical system).
2. Use computation to find and evaluate a model.
3. Use theory, analysis, and computation to derive a consequence of the model.

### Optimization problems
Every optimization problem has two parts:

1. An objective function that will either be maximized or minimized (e.g., "get a minimum fare between Paris and London")
2. A set of constraints that must be satisfied (e.g., "travel cannot take longer than 6 hours")

*Problem reduction* is the process of modifying a problem to resemble a problem that we already know how to solve. Optimization problems are often polynomial time (i.e., there is no computationally efficient way to solve them); approximations often used.

#### Knapsack problem
A burglar is robbing a home (maximize monetary value) with a limited ability to take away items (weight).

					value	weight	value/weight
	clock			175		10		17.5
	painting
	radio
	...

*Greedy algorithm* is iterative and at each step you pick the locally optimal solution. Take the highest value-weight item, check if can carry more, add next best item, etc. In this case, no solution (pick lightest, pick most expensive, pick highest ratio) provides the optimal solution.

Referred to as "0/1 Knapsack problem" since items cannot be cut in half (can be taken or  not taken).

**How do we choose the absolute optimal set?** Assign the `<value, wieght>` of each item, designate `w` as max weight, and `I` as vector of available items and `V` of items taken.

	maximize: 		sum of (V[i] * I[i].value)
	subject to:		(sum of (V[i] * I[i].weight)) ≤ w
	
Implementations: 1) enumerate all possibilities and choose best that meets constrain (brute force),  2) ???. Brute force will take 2^n possibilities.