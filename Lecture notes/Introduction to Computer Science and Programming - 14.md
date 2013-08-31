# Introduction to Computer Science and Programming
## Lecture 14

### Probability
How do we determine the probability of rolling a dice ten times and not rolling a one? There are 6^10 possible combinations. How many don't contain one? The probability on the first roll is 5/6 (as is for every other roll, since each is independent). Therefore, the probability of not getting a one is (5/6)^10. The probability of rolling at least one one is 1-((5/6)^10).

It is many times easier to determine the opposite of what you wish to determine the probability of, and subtracting it from one.

Pascal is the founder of probability theory.

In 24 double rolls, what are the changes of getting two sixes in a row? The probability of two sizes is (1/6 * 1/6 = 35/36). Therefore, the answer is: (35/36)^24. We can perform trials, and come close to this number. Sometimes it's easier to run simulations, other times it's easier to determine analytically.

### Simulations & Statistics
The simluation for the dice game is a *Monte Carlo simulation*, a statistical method. This technique was used successfully during the Manhattan Project. It's an example of *inferential statistics*—premised that a random sample tends to exhibit the same properties as the population from which it is drawn. Problem: It's a difficult assumption; you need to ensure the sample is not biased.

#### Sample sizes
Flipping a coin? Confident in one toss heads? Two tosses heads? Hundred? (Rigged coin.) What about 48 heads, 52 tails? It's not possible to tell. You can re-run simulations on similar sample sizes to determine how reliable the outcome/output is.

The *law of large numbers* states repeated independent tests with the same actual probability P chance that the fraction of times that outcome occurs converges to P as the number of trials approaches infinity. This is related to the *gambler's fallacy* (at roulette table, after twenty hits on black: "Red is due!").

> In probability theory, the law of large numbers (LLN) is a theorem that describes the result of performing the same experiment a large number of times. According to the law, the average of the results obtained from a large number of trials should be close to the expected value, and will tend to become closer as more trials are performed.

You can graph this convergence to better appreciate it. (Be careful of drawing lines between data points; it can make it look like a trend, where no such trend occurs.) You can use log-scales to gain greater insight into smaller differences on the graph.