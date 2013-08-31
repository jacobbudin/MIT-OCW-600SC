# Introduction to Computer Science and Programming
## Lecture 9

### Memory allocation
If every integer takes 4 units of memory and we know the start of the list, then the position  of the desired interger is `start+4*i`. (This is true of 32-bit, 64-bit, etc., very large integers are supported and the same size.) What about not fixed sizes (e.g., strings)? (Many programming languages enforce same-type lists. Obviously, Python does not.)

In *linked lists*, the pointer to the next value is the first point of the previous value. At the end of the lists, the pointer points to a null-type value. In Python (and all other object-oriented programming languages), *indirection* is used: the pointers and objects are separated. The pointers are the list. The objects are scattered. The caveat: The objects may be far apart, disrupting cache, and destroying efficiency.

### Binary search (returns)
Binary search depends on a sorted list. How do we sort the list? Does it make sense to sort the list? (Binary search computes in log^n, regular search is n.) There is no regular list can be sorted faster than linear time (O(n)).

Why use binary search at all? Because we are often interested in *amorized complexity*: sort once, search many times (the time cost of the sort can be allocated to each of the searches). The cost comparison needs to take into account the number of searches  performed and the time cost of sorting.

### Sorting lists
*Bubble sort* is the wrong answer. *Selection sort* is better and simple. It depends on establishing and maintaining an *invariant* (something that is invariably true). Prefix and suffix. The invariant is that the prefix is sorted.

It scans the rest of the list (suffix) and swapping the current pointer with the smallest number found (adding one to the prefix) and moving along.

#### Divide and conquer
Basic concepts:

1. Minimize problem to lowest thresold input size
2. Divide the problem
3. Merge the subsolutions

If given two sorted lists, you can merge them quickly. You do comparisons between each of the "remaining" first pointers. This can be done in linear time.

Division is done (e.g., 24 items): 12 lists with 2 items, 6 lists with 4 items, 3 lists with 8 items. The depth of recusion is log^n.