# Introduction to Computer Science and Programming
## Lecture 17

Correction to lecture 16: Small standard deviation indicates a reliable answer: it does not. The simulation may be wrong; the conceptual model must be correct (and it must be correctly implemented). Tests must be done to ensure correctness/truth.

### Scientific modelling process
You start with a 1) *physical situation*. Then build a 2) *theoretical model*. When complexity prevents additional theoretical models, 3) *computational models* are added.

#### Modelling errors
We need to assume some *perturbation* of data. Data is normally distributed, a Gaussian distribution. For example, springs: [Hooke's law](http://en.wikipedia.org/wiki/Spring_(device)#Hooke.27s_law) `f = -kx` (linear force for most materials), but springs have elastic limits. (The negative indicates the force is in the opposite direction.)

Testing a spring once may have errors; therefore, do a series of experiments testing with multiple weights. Graph the results; find slope of line to determine `k`.

#### Line fitting
With two points, it's easy. For multiple points, there needs to be an objective fit for determing best fit: *the least squares fit*.

	sum of (observed[i] - predicted[i])^2
	
Pylab does it for you with the `polyfit(obsX, obsY, degree)` function. This is *linear regression*, can be used to find polynomials other than lines.

You can use values you don't know the answers to to determine the predictive value of a model. (In this case, a cubic function appears to fit better, but does not work for larger predictive values. Linear function is correct, but large values may exceed the elastic limit set out in Hooke's law. Removing final values achieves a better fit.)

#### Measuring different fits
Calculate mean square error of the various fits. Problem: There's a lower bound of zero, but not an upper bound. Instead: use *coefficient of determination* (R^2):

	R^2 = 1 - (estimated error) / (measure of variance)
	
R^2 is always between zero and one.