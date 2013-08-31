# Introduction to Computer Science and Programming
## Lecture 16

### Computational models
How do we build computational models that reflect the real-world? In the case of fair dice, the chance of any given number is equal therefore it makes up a *uniform distribution*—that is, each result is equally likely. Uniform distributions are common in games, not in nature. *Exponential distributions* are used to model continuous distributions that are memoryless (e.g., the concentration of a drug in the human body). That is, whether a given module gets cleared is independent of the previous occurance of clearings (exponential decay).

	P = probability of molecule surviving
	T = time
	(1-P)^T

Note: You can check for exponential growth and decay by plotting the Y-axis on a logarithmic scale and checking for a straight line.

Two options: You could calculate with analytic model, as above, or a simulation model (e.g., a Monte Carlo simulation) to create the randomness indicated. Monte Carlo simulations will not produce the "exactness".

*Fidelity-credibility*—is the model believable?  
*Utility*—what's answerable with the model?

### Monte Hall problem
Based on "Let's Make a Deal!": 3 doors, one has big prize. Monte Hall brings contestant to floor and asks him to choose a door. They open a door that has a junk prize. Monte asks if the contestant wants to switch doors. Should he? It's very contentious.

It *does* matter! Monte always opens the door of a junk prize; his choice is not independent of the choice of the player. Monte cannot pick the door of player. Switching doubles the odds of winning. Run a Monte Carlo simulation to prove it.

### Randomization's role
Randomization is used in problems that do not have a random element. For example, to calculate pi, randomly drop needles on circle on top of square. Use randomness to "drop needles"—in larger experiments, standard deviation drops.