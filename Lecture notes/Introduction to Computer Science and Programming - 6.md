# Introduction to Computer Science and Programming
## Lecture 6

### Other dictionary features
Keys can be tuples, coordinates, etc.—all immutable structures. Dictionaries could be implemented as lists, but the lists have to be searched by key. Dictionary key values can be retrieved constantly, regardless of size, thanks to its hashing mechanism. Lists increase linearly with size.

### Divide & conquer technique
The *divide & conquer technique* involves taking a hard problem, spliting them into small problems, and solving small problems.

### Recursion
*Recursion* is a way of characterizing a problem and designing solutions. It is an example of divide and conquer. A *base case* provides a direct answer. [Towers of Hanoi](http://en.wikipedia.org/wiki/Towers_of_hanoi#Recursive_solution) solutions and palindrome determination are good examples of problems with simpler recursive solutions.

### Fibonnaci sequence
The Fibonnaci sequence was originally intended to estimate the population growth of rabbits (one pair per female per month). The base case is the values of 0,1 equals 1, otherwise add the last two subsequent populations to arrive at the current population (in months).