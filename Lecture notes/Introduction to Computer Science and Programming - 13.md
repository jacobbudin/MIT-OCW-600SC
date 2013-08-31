# Introduction to Computer Science and Programming
## Lecture 13

### Drunkard's walk (continued)
What was wrong with the walk? There was a misplacement of arguments in the code. The answers are much easier interpreted with visualizations. Running the simulation again will cause different results. This is a *stochastic system*:

> In probability theory, a stochastic system is one whose state is non-deterministic. The subsequent state of a stochastic system is determined both by the system's predictable actions and by a random element. A stochastic process is one whose behavior is non-deterministic; it can be thought of as a sequence of random variables. Any system or process that can be analyzed using probability theory is stochastic.

The Copenhagen doctrine suggested that the deterministic systems do not occur in the natural world. *Causal non-determination* that the past actions do not predict the future; randomness is naturally occuring. Oppositely, *predictive non-determination* is that our understandings of the current states are imperfect, which means we cannot know the future with certainty. (This is an unsettled debate in science.)

*Stochastic processes* are those whose outcome depend on the previous state and some random element. In Python, we use `random.choice`. All random fuctions in Python  use `random.random` that generate a floating integer between zero and one.

In dice games, each roll is independent of the previous roll.

### Visualization
[pylab](http://www.scipy.org/PyLab) can be used to graph plots. It's similar to but simpler than [matplotlib](http://matplotlib.org).

	import pylab
	pylab.plot([1,2,3,4], [1,2,3,4])
	pylab.plot([1,4,2,3], [5,6,7,8])
	#pylab.title('5% Growth, Compounded Annually')
	#pylab.xlabel('Years of Compounding')
	#pylab.ylabel('Value of Principal ($)')
	pylab.show()
