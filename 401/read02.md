# In Tests We Trust - TDD with Python

The programmers talking about two things: refactoring and unit tests, In here we will talk about tests

In Summary. “Unit testing” is writing many small tests that each test one very simple function or object behavior. TDD is a thinking process that results in unit tests, and “thinking in tests” tends to result in more fine-grained and comprehensive testing, and an easier-to-extend software design.


TDD is a software development technique that melds program design, implementation, and testing in a series of micro-iterations that focus on simplicity and feedback. Programmer tests are created using a unit testing framework and are 100% automated.


## The Cycle

The cycle of TDD is made by three steps:
* Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
* Write the feature and make the test pass! (you can dance after that)
* Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)


## TDD steps
we need to think about tests first.
Coming back to the code and thinking with baby steps, what is the smaller test that we can do against a function (method/class) that will return the gender?
Just recaping: we have a name as input and we need to return a gender as output. So, the smaller test is: given a name, return a gender.
![test](https://miro.medium.com/max/875/1*gxEKnrQuS7CO3hONTD7_hg.png)


## some tips
The greatest advantage about TDD is to craft the software design first
Your code will be more reliable: after a change you can run your tests and be in peace
Beginning may be hard — and that’s fine. You just need to practice!


# If name equals main

## What does the if __name__ == “__main__”: do?
Simply , If u want to run the code from the main file you should call the functions inside if __name... and be sure anything inside it will not work when imported from other files 

example:

```
# Suppose this is foo.py.

print("before import")
import math

print("before functionA")
def functionA():
    print("Function A")

print("before functionB")
def functionB():
    print("Function B {}".format(math.sqrt(100)))

print("before __name__ guard")
if __name__ == '__main__':
    functionA()
    functionB()
print("after __name__ guard")
```

```
# What gets printed if foo is the main program
before import
before functionA
before functionB
before __name__ guard
Function A
Function B 10.0
after __name__ guard

```
```
# What gets printed if foo is imported as a regular module
before import
before functionA
before functionB
before __name__ guard
after __name__ guard

```

# Recursion
Recursion is a programming technique where a method can call itself as part of its calculation (sometimes you can have more than one method - the methods would then normally call each other circularly).
![rec](https://cdn.programiz.com/cdn/farfuture/6i17bRQT6hWIqw9JE5rMMyW527g7It_68T7kSzpIplo/mtime:1591262415/sites/tutorial2program/files/python-recursion-function.png)
Basically, a function is recursive when
A function has a simple base case, and when
All other cases have rules which reduce to the base case.
As an example, 


```
def factorial(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1:
        return 1
    else:
        return (x * factorial(x-1))


num = 3
print("The factorial of", num, "is", factorial(num))

```
Output
```
The factorial of 3 is 6
```