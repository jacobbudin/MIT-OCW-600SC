# Introduction to Computer Science and Programming
## Lecture 10

### Hashing
*Hashing* converts values to another value in some range. This range is ordered (we can find a value in an ordered list in constant time). The linking is called a "bucket". Hashing is how dictionaries are implemented in Python. They are very efficient in time (less so, space).

The hash function is many-to-one. A *collision* occurs when multiple objects map to the same hash. Greater numbers of buckets result in fewer collisions. A good hash function widely disperses values among buckets. If enough space is allocated, look-up can be done in constant time. (Otherwise, it's linear time.)

Any kind of immutable object can be hashed.

### Exceptions
An *exception* is an error. An *unhandled exception* causes the program to crash. Exceptions are a valuable control-of-flow concept. Exceptions are written in `try`/`except` blocks. They are frequently used for user input.

### Classes
A *module* (e.g., `math`) is a collection of related functions. It uses dot notation (`math.log`) to avoid name conflicts. A class is a collection of data and functions, called attributes. Classes are the basis of object-oriented programming.

A *message passing metaphor* is a look-up from class to method, which executes it on the object (e.g., `c.area()` pass the message `area` to `c`). A *method* is a function associated with an object. `list` and `dict` are built-in classes.