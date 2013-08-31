# Introduction to Computer Science and Programming
## Lecture 7

### Binary numbers
Everything is represented as 0 and 1.

In base 10:

	304 = 3*100 + 0*10 + 4*1 = 304

In base 2:

	101 = 1*4 + 0*2 + 1*1 = 5
	
Size is 2^n. Computers work in base 2 because it's easy to build switches in electronic hardward. Switches have two possible positions: on and off. Computers have difficultly representing decimals, e.g. 0.125 in base 10:

	0.125 = 1*.1 + 2*.01 + 3*.001 = 0.125
	
In  base 2, the answer for 0.1 is infinite (`bin(0.1)` breaks). Answer: Uses approximation. `print`-ing will round to 17 digits. Does it matter? Usually, no. Checking for equality with these approximations will fail due to the sacrfices of floating-point arithmetic. 

**Moral of the story:** Don't test whether two floating points are equal to one another, check to see whether values are within a very small tolerance.

### Debugging
The goals of debugging is not to eliminate one bug quickly, but to move towards a bug-free program. Most debugging relies on merely `print`-ing, but specific tools for debugging exist. Be systematic; use an approach like binary search. Don't ask what went wrong, ask:

> How could it have produced the result it did?

1. Study available data.
2. Generate test results for more data to study.
3. Form a hypothesis consistent with data.
4. Design and run a repeatable experiment that has the potential to refute the hypothesis.
