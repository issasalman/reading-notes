# FUNCTIONAL PROGRAMMING

## What is functional programming?

Functional programming means using functions to the best effect for creating clean and maintainable software. This article illustrates the concepts behind the functional paradigm with practical examples in JavaScript and Java.

## What is a pure function and how do we know if something is a pure function?
In programming, a pure function is a function that has the following properties:
1. The function always returns the same value for the same inputs.
2. Evaluation of the function has no side effects. Side effects refer to changing other attributes of the program not contained within the function, such as changing global variable values or using I/O streams. 

Effectively, a pure function’s return value is based only on its inputs and has no other dependencies or effects on the overall program.

## What are the benefits of a pure function?
Pure functions are much easier to read and reason about.

## What is immutability?
the state or condition of being unchangeable

## What is Referential transparency?

Referential Transparency emphasizes that an expression in a JavaScript program may be replaced by its value or any other variable having the same value without changing the result of the program.

## What is a module?
A module is a software component or part of a program that contains one or more routines. One or more independently developed modules make up a program.


## What does the word ‘require’ do?
the builtin require function is the easiest way to include modules that exist in separate files. The basic functionality of require is that it reads a JavaScript file, executes the file, and then proceeds to return the exports object. An example module:

## How do we bring another module into the file the we are working in?
To include functions defined in another file in Node.js, we need to import the module. we will use the require keyword at the top of the file.

The result of require is then stored in a variable which is used to invoke the functions using the dot notation.

To see that in action, let’s import the lib.js module by requiring it inside the main.js file and invoke the add() function with dot notation.



## What do we have to do to make a module available?
we need to export the module from the file where it exists.