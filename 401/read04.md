# Classes and Objects & Thinking Recursively

## Classes and Objects
* Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes.

* Classes are essentially a template to create your objects.

A very basic class would look something like this:

```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")
```    

# Thinking Recursively
Recursion occurs when a thing is defined in terms of itself. The most common application of Recursion is in Mathematics and Computer Science.

## What is Recursive Function in Python?
In Python, we know that a function can call other functions. It is also possible for the function to call itself. These types of functions are known as Recursive Function.

Every Recursive Function must follow 3 main conditions.
Base Case or Base Condition
Recursive Call
Action

## Advantages of Recursive Functions
If we wants to make our code look elegant and neat, recursive functions make sure of that.
A complex operation can be divided into similar sub-problems using recursion.
Recursive Functions are more useful in ‘Sequence Generation’ problems.

## Disadvantages of Recursive Functions
It is hard to debug recursive functions.
Sometimes the logic behind recursive function is little difficult to follow.
They takes up a lot of space and time while executing.
Before we wind up, let’s take a look at another example for better

## Conclusion
Recursive functions make our program more elegant and it’s also easy to write once you get the hang of it, but they have their share of drawbacks too.
So, use them wisely and make sure you define the base condition.

# Python Testing with pytest: Fixtures and Coverage
In testing, a fixture provides a defined, reliable and consistent context for the tests. This could include environment (for example a database configured with known parameters) or content (such as a dataset).

Fixtures define the steps and data that constitute the arrange phase of a test (see Anatomy of a test). In pytest, they are functions you define that serve this purpose. They can also be used to define a test’s act phase; this is a powerful technique for designing more complex tests.

The services, state, or other operating environments set up by fixtures are accessed by test functions through arguments. For each fixture used by a test function there is typically a parameter (named after the fixture) in the test function’s definition.

We can tell pytest that a particular function is a fixture by decorating it with @pytest.fixture. Here’s a simple example of what a fixture in pytest might look like:

```
import pytest


class Fruit:
    def __init__(self, name):
        self.name = name

    def __eq__(self, other):
        return self.name == other.name


@pytest.fixture
def my_fruit():
    return Fruit("apple")


@pytest.fixture
def fruit_basket(my_fruit):
    return [Fruit("banana"), my_fruit]


def test_my_fruit_in_basket(my_fruit, fruit_basket):
    assert my_fruit in fruit_basket
```


Coverage.py measures code coverage, typically during test execution. It uses the code analysis tools and tracing hooks provided in the Python standard library to determine which lines are executable, and which have been executed.

$ pip install coverage

$ coverage run -m pytest fileName

$ coverage report -m
```
Name                      Stmts   Miss  Cover   Missing
-------------------------------------------------------
my_program.py                20      4    80%   33-35, 39
my_other_module.py           56      6    89%   17-23
-------------------------------------------------------
TOTAL                        76     10    87%
```
For a nicer presentation, use coverage html to get annotated HTML listings detailing missed lines:

$ coverage html