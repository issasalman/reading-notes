# Dunder Methods

## What Are Dunder Methods?

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:

```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
To fix this, you can add a __len__ dunder method to your class:

class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42

```

### Object Initialization: __init__
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:

### Object Representation: __str__, __repr__
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1- __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

2- __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

# Python Statistics & Probability Theory

The first topic that you should probably tackle is statistics and probability theory. There are not only quite some videos and courses out there that can help you, but there are also a lot of (printed) books that will help you to get started with statistics in Python.

### Probability Theory with Python

Probability theory is also something that is highly valuable to take into account when you’re learning statistics with Python. It’s the analysis of random phenomena. That means that the outcome of any random event is non-deterministic: it can be any of the several possible outcomes, and the eventual outcome is determined by chance.

### Choosing Python Statistics Libraries
There are many Python statistics libraries out there for you to work with, but in this tutorial, you’ll be learning about some of the most popular and widely used ones:

1- Python’s statistics is a built-in Python library for descriptive statistics. You can use it if your datasets are not too large or if you can’t rely on importing other libraries.

2- NumPy is a third-party library for numerical computing, optimized for working with single- and multi-dimensional arrays. Its primary type is the array type called ndarray. This library contains many routines for statistical analysis.

3- SciPy is a third-party library for scientific computing based on NumPy. It offers additional functionality compared to NumPy, including scipy.stats for statistical analysis.

4- Pandas is a third-party library for numerical computing based on NumPy. It excels in handling labeled one-dimensional (1D) data with Series objects and two-dimensional (2D) data with DataFrame objects.

5- Matplotlib is a third-party library for data visualization. It works well in combination with NumPy, SciPy, and Pandas.