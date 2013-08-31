# Introduction to Computer Science and Programming
## Lecture 3

### Find cube root algorithm
The type of algorithm is guess-and-check (specifically, exhuastive enumeration). This is a brute force solution. These solutions "work" because of the speed of modern computers.

### Approximation
Approximation is finding an answer that's "good enough" (one within a range of epsilon). Approximation is appropriate if the specification allows. Algorithmic complexity depends on the width of tolerance.

### Improving square root algorithm
Bisecting algorithms choose the value that bisects the range of possible values and then removes one-half of the values (that all produce values too high or too low). Produces algorithm of log2 complexity.

For instance, from 1 to 100. There 100 values to search. In bisecting, 6.64 values.

