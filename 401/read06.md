# Game of Greed 1

##  Random Module 

The random module is a built-in module to generate the pseudo-random variables. It can be used perform some action randomly such as to get a random number, selecting a random elements from a list, shuffle elements randomly

### Some Methods in Random Module
1. random.random()
```
>>> import random
>>> random.random()
0.645173684807533

```
2. random.randint()
```
>>> import random
>>> random.randint(1, 100)
95           
>>> random.randint(1, 100)
49
```

3. random.randrange

```
>> random.randrange(1, 10)
2
>>> random.randrange(1, 10, 2)
5            
>>> random.randrange(0, 101, 10)
80
```

4. random.choice()

```
>>> import random
>>> random.choice('computer')
't'          
>>> random.choice([12,23,45,67,65,43])
45           
>>> random.choice((12,23,45,67,65,43))
67
```

5. random.shuffle()

```
>>> numbers=[12,23,45,67,65,43]
>>> random.shuffle(numbers)
>>> numbers
[23, 12, 43, 65, 67, 45]
>>> random.shuffle(numbers)
>>> numbers
[23, 43, 65, 45, 12, 67]
```

## What is Risk Analysis
In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

## the possible risks that you may encounter

- Use of new hardware
- Use of new technology
- Use of new automation tool
- The sequence of code
- Availability of test resources for the application

## How to perform Risk Analysis?
### There are three steps:

- Searching the risk

- Analyzing the impact of each individual risk

- Measures for the risk identified


## What is Code Coverage
![code coverage](https://martinfowler.com/bliki/images/testCoverage/sketch.png)
What is Code Coverage? Code coverage is the percentage of code which is covered by automated tests. Code coverage measurement simply determines which statements in a body of code have been executed through a test run, and which statements have not. ... This loop will continue until coverage meets some specified target.

## How Code Coverage Works
There are many approaches to code coverage measurement. Broadly there are three approaches, which may be used in combination:

Source code instrumentation
This approach adds instrumentation statements to the source code and compiles the code with the normal compile tool chain to produce an instrumented assembly.

Intermediate code instrumentation
Here the compiled class files are instrumented by adding new bytecodes, and a new instrumented class is generated.

Runtime information collection
This approach collects information from the runtime environment as the code executes to determine coverage information.