# Introduction to Computer Science and Programming
## Lecture 12

### Classes (continued)
You shouldn't access object properties directly, unless it's necessary. `yield` is a generator. In `return`, the value pops off the stack. But `yield` is a function that remembers the point the function body where it last returned, plus all of the local variables. `yield` provides more control.

### Computational models
For much of history, science has tried to build *analytic methods* to predict behavior given initial conditions and parameters. Recently, *simulation methods* have become predominate, because A) problems that are not mathematically tractable, B)as problems become more complicated, successfully refining a series of simulations, C) extract useful intermediate results, and D) computers.

Simulation methods build models with useful information about the behavior of the system, and provides an approximation to reality. Simulation models are *descriptive*. Analytic models are *prescriptive*.

#### Random walk
*Brownian motion* (e.g., floating pollen in water) is a *random walk*; how do we model it? This is useful in modelling physical processes and social conditions. For instance, a drunk university student who's in a large field; every second the student can make one step in a cardinal direction (N, E, S, W). Obvious guess: end up where he started.

After one step, 1 unit away is 100%. After 2 steps : 0 unit away (25%), root 2 units away (50%), 2 units away (25%). After 3 steps: 1 unit away (25%), etc.

	- 1 step: 1 unit away
	- 2 steps: 1.2071 units away
	- 3 steps: 1.4xxx units away

This can be modeled with a drunk, a field, and a location. Using `random.choice` of `[[0,1], [0, -1], [1, 0], [-1, 0]]`, you can simulate the coordinate-based being drunk. There are some assumptions: the field is flat, drunks can't run into each other, etc.