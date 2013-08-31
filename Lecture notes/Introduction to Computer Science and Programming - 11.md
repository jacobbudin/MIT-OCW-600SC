# Introduction to Computer Science and Programming
## Lecture 11

### Classes
Classes are *abstract data types*. They are abstract in the sense that we provide the interface, a *specification*, that explains what the methods do (not how they do it). Names with `__` as part of their name have special meaning in Python. The `__init__` is the constructor in Python. Data hiding (such as PHP and Java) helps obscure class functionality that cannot be altered without affecting the class. It does so by preventing direct access to *instance variables* (one copy per object) and *class variables* (one copy per class). Python does not have data hiding.

#### Inheritance
Classes that inherit have all the attributes of a parent ("super") class, but those attributes can be overwritten.