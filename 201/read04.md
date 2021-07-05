## Lists
![list](https://image.slidesharecdn.com/5-listseng-130502080952-phpapp01-130504015816-phpapp01/95/html-list-1-638.jpg?cb=1367632899)
There are three different types:-
1. Ordered List
2. Unordered List 
3. Definition Lists

Ordered and unordered lists contains ``<li>`` tag but Definition Lists contain `` <dl> <dt> <dd>`` tags  
exmaple
```
<dl>
<dt>Sashimi</dt>
<dd>Sliced raw fish that is served with 
 condiments such as shredded daikon radish or 
 ginger root, wasabi and soy sauce</dd>
<dt>Scale</dt>
<dd>A device used to accurately measure the 
 weight of ingredients</dd>
<dd>A technique by which the scales are removed 
 from the skin of a fish</dd>
 </dl>

 ```
 dt for (the definition term while dd  used to contain the 
definition.

There can be nested lists and the parent has different shape than its child
 

![2](https://media.geeksforgeeks.org/wp-content/uploads/Screen-Shot-2017-11-22-at-1.53.16-AM.png)

## Boxes
* Controlling size of boxes
* Box model for borders, margin and padding
* Displaying and hiding boxes

Box Dimensions
 Dimensions can be change by changing pixels, percentages, or 
ems, Most uses pixels for accurately size but for now Designers 
have recently started to use 
percentages and ems more for 
measurements as they try to 
create designs that are flexible 
across devices which have 
different-sized screens.

Limiting Width by  

min-width: 450px;
max-width: 650px;

Limiting height by  

min-height: 10px;
max-height: 30px; 

overflowing content by 

overflow: hidden; Will hide the text 
overflow: scroll; Will make scroll button

## Border, Margin & Padding

1. Border 

Every box has a border (even if 
it is not visible or is specified to 
be 0 pixels wide). The border 
separates the edge of one box 
from another

2. Margin 

Margins sit outside the edge 
of the border. You can set the 
width of a margin to create a 
gap between the borders of two 
adjacent boxes

3. Padding 

Padding is the space between 
the border of a box and any 
content contained within it. 
Adding padding can increase the 
readability of its contents

## ARRAYS
![w](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSSR5wrFxDtRGxzXaJQ8y2eFI2kJSoWbjdPPw&usqp=CAU)
An array is a special type of variable. It doesn't 
just store one value; it stores a list of values.

Values in an array are accessed as if they are in 
a numbered list. It is important to know that the 
numbering of this list starts at zero (not one).

## switch statemen
A switch statement starts with a 
variable called the switch value. 
Each case indicates a possible 
value for this variable and the 
code that should run if the 
variable matches that value.

![2](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS1XgsmDwkOOlOUjBGFYb6jpasYCJqXH3HaOQ&usqp=CAU)


Conditional statements allow your code to make 
decisions about what to do next. 
Comparison operators (===, ! ==, ==, ! =, <, >, <=, =>) 
are used to compare two operands. 
Logical operators allow you to combine more than one 
set of comparison operators. 
if ... else statements allow you to run one set of code 
if a condition is true, and another if it is false. 
switch statements allow you to compare a value 
against possible outcomes (and also provides a default 
option if none match). 
Data types can be coerced from one type to another. 
All values evaluate to either truthy or falsy. 
There are three types of loop: for, while, and 
do ... while. Each repeats a set of statements.