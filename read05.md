# Expressions and operators
## Operators
JavaScript has the following types of operators. This section describes the operators and contains information about operator precedence.
![operators](https://miro.medium.com/max/2560/1*KEQpF2Ud3D9yfNKmaBgD9A.jpeg)

1. Assignment operators
2. Comparison operators
3. Arithmetic operators
4. Bitwise operators
5. Logical operators
6. String operators
7. Conditional (ternary) operator
8. Comma operator
9. Unary operators
10. Relational operators


![loops](https://www.tutsmake.com/wp-content/uploads/2020/05/Loops-In-JavaScript.jpeg)

## Loops and iteration

``for statement
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

A **for statement** looks as follows:

for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement``

   **while statement**  
``while statement
A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

while (condition)
  statement
Copy to Clipboard
If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.``

``**Examples**    
**While loop **  
let n = 0;  
let x = 0;  
while (n < 3) {  
  n++;  
  x += n;  
}
![loops](https://media.geeksforgeeks.org/wp-content/uploads/20191108131134/For-Loop.jpg)
     **For loop**  
fruits = ["apple", "banana", "cherry"]  
for x in fruits:  
  print(x)  
  if x == "banana":

``