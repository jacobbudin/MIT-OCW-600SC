# Introduction to Computer Science and Programming
## Lecture 8

### Efficiency
Efficiency is rarely about clever coding, but choosing the right algorithm. Algorithms are difficult to build, so reduce it to a previously solved problem. There are two metrics of efficiency: speed and time. *Computational complexity* is not measured in minutes because of effects of the speed of the machine, cleverness of programming language implementation, and variability of input. Instead, count the number of basic steps.

	T:N -> N
	
First N is size of input. Second N is number of steps. Steps can take constant time. In a *Random Access Machine (RAM)*, steps are done sequentially and memory acccess is in constant time. (Modern computers are more complex and have various levels of memory.)

#### Best and worst case
The best case is the minimum time required. The worst case is the maximum time required. The expected case is what would happen most of the time, but it's complex to determine without developing a model (e.g., in a list: what kind of queries? what kind of distribution of values?). Complexity analysis almost always focuses on worst case. Worst case is the upper bound and often happens (e.g., a value does not exist in a list).

#### Calculating complexity
Two assignments, a loop with three assignments, a return:

	2 + 3n + 1
	
Ignore constants (`2` and `1`), because concern is growth with respect to size. Also ignore multiplicative growth (`3`). Big O notation is used to express it. Example:

	F(x) = O(x^2)
	
Function F grows no faster than the quadratic polynomial x^2. More examples

	O(1)			constant
	O(log n)		logarithmic
	O(n)			linear
	O(n log n)		lug linear
	O(n^c)			polynomial
	O(c^n)			exponential

In computing complexity where adding digits of integer:

	log 10 (x)
	
Binary search:

	log 2 (x)