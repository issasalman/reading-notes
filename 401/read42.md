# Pythonisms

## What Are Dunder Methods?
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__ or __str__.`

## Special Methods and the Python Data Model
Special Methods and the Python Data Model
This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code, knowing how and when to use dunder methods is an important step.

## Enriching a Simple Account Class

Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:

* Initialization of new objects
* Object representation
* Enable iteration
* Operator overloading (comparison)
* Operator overloading (addition)
* Method invocation
* Context manager support (with statement)

`Object Initialization: __init__`


`Object Representation: __str__, __repr__`

```
__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.
```
```
Context Manager Support and the With Statement: __enter__, __exit__
```
My final example in this tutorial is about a slightly more advanced concept in Python: Context managers and adding support for the with statement.

Now, what is a “context manager” in Python? Here’s a quick overview:

A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all you need to do is add __enter__ and __exit__ methods to an object if you want it to function as a context manager.

Let’s use context manager support to add a rollback mechanism to our Account class. If the balance goes negative upon adding another transaction we rollback to the previous state.

## Python Iterators That Iterate Forever

Python Iterators That Iterate Forever
We’ll begin by writing a class that demonstrates the bare-bones iterator protocol in Python. The example I’m using here might look different from the examples you’ve seen in other iterator tutorials, but bear with me. I think doing it this way gives you a more applicable understanding of how iterators work in Python.

## How do for-in loops work in Python?
As you can see, the for-in was just syntactic sugar for a simple while loop:

It first prepared the repeater object for iteration by calling its __iter__ method. This returned the actual iterator object.
After that, the loop repeatedly calls the iterator object’s __next__ method to retrieve values from it.

## A Simpler Iterator Class
Remember why we needed the RepeaterIterator class again? We needed it to host the __next__ method for fetching new values from the iterator. But it doesn’t really matter where __next__ is defined. In the iterator protocol, all that matters is that __iter__ returns any object with a __next__ method on it.

## Python Iterators – A Quick Summary
Iterators provide a sequence interface to Python objects that’s memory efficient and considered Pythonic. Behold the beauty of the for-in loop!
To support iteration an object needs to implement the iterator protocol by providing the __iter__ and __next__ dunder methods.
Class-based iterators are only one way to write iterable objects in Python. Also consider generators and generator expressions.

## Python Generators –
* Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
* The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
* Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.