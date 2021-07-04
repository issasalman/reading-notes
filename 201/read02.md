# Text in HTML
We will take about 3 main topics
*  Headings and paragraphs
* Bold, italic, emphasis
* Structural and semantic markup
![htmltext](https://i.ytimg.com/vi/8bZ4RPjOPYE/maxresdefault.jpg)
In this chapter we focus on how to add markup to the text that 
appears on your pages. You will learn about:  
* Structural markup:
 the elements that you can use to 
describe both headings and paragraphs  
* Semantic markup:   
which provides extra information; such 
as where emphasis is placed in a sentence, that something 
you have written is a quotation (and who said it), the 
meaning of acronyms, and so on.

To create a text inside HTML u can do it in many ways using different tags like:  
1. Headings 
2. paragraphs
3. superscript and subscipt
and other tags like
1. Bold & Italic
2. Line Breaks & 
Horizontal Rules
3. Strong & Emphasis
4. quotations:
5. citations & Definitions   


`
# Introducing CSS

In this section, we will look at how to 
make your web pages more attractive, 
controlling the design of them using CSS.

  CSS works by associating rules with HTML elements. These rules govern 
how the content of specified elements should be displayed. A CSS rule 
contains two parts: a selector and a declaration.

Selectors   
 indicate which 
element the rule applies to. 
The same rule can apply to 
more than one element if you 
separate the element names 
with commas.  

![selctor](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics/css-declaration-small.png)

Declarations    

 indicate how 
the elements referred to in 
the selector should be styled. 
Declarations are split into two 
parts (a property and a value), 
and are separated by a colon

CSS declarations sit inside curly brackets and each is made up of two 
parts: a property and a value, separated by a colon. You can specify 
several properties in one declaration, each separated by a semi-colon.

We can add a style to html using css by three ways
1. external css file
2. inline style
3. internal style 

# Basic Javascript instructions
A script is a series of instructions that a computer can follow one-by-one. 
Each individual instruction or step is known as a statement. 
Statements should end with a semicolon.  
JAVASCRIPT IS CASE SENSITIVE   
JavaScript is case sensitive so hourNow means 
something different to HourNow or HOURNOW. 

You should write comments to explain what your code does. 
They help make your code easier to read and understand. 
This can help you and others who read your code. 
1. MULTI-LINE COMM ENTS 
To write a comment that stretches over more than 
one line, you use a multi-line comment, starting with 
the /* characters and ending with the */ 

2. SINGLE-LINE COMMENTS 
In a single-line comment, anything that follows the 
two forward slash characters I/

A script will have to temporarily 
store the bits of information it 
needs to do its job. It can store this 
data in variables.

## DATA TYPES
1. DATA TYPES 
2. STRING DATA TYPE 
3. STRING DATA TYPE 
![w](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-data-types.jpg)

## RULES FOR NAMING VARIABLES 
* The name must begin with 
a letter, dollar sign ($),or an 
underscore (_). It must not start 
with a number.  
 * The name can contain letters, 
numbers, dollar sign ($), or an 
underscore (_). Note that you 
must not use a dash(-) or a 
period (.) in a variable name 
 * You cannot use keywords or 
reserved words. Keywords 
are special words that tell the 
interpreter to do something. For 
example, var is a keyword used 
to declare a variable. Reserved 
words are ones that may be used 
in a future version of JavaScript. 

## OPERATORS




1. ASSIGNMENT OPERATORS 
2. COMPARISON OPERATORS 
3. ARITHMETIC OPERATORS
4. LOGICAL OPERATORS
5. STRING OPERATORS 

# Decisions and loops 

![q](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSKJm2Wt14c_nLivYVMzXyG0c3gK3g0mNbGuw&usqp=CAU)

JavaScript supports the following types of if else statement −

     if statement
     if else statement
     if else if statement.
if statement

 if statement is the statement that enables JavaScript to make decisions

and execute statements only if condition is true.

Syntax:

The syntax for a if statement is as follows –

if(expression)
{
    block of code is executed if the expression is true
}
In the above syntax if the expression is true the block of code will get

executed and if expression is not true then nothing will be executed. Most

of the time comparison operators are used while making decisions.

Following is an example of if statement:

Code Implementation
```
<html>

   <body>
      
      <script type='text/javascript'>

         <!--

            var student_age = 22;
     

            if( student_age > 10 ){ 
               document.write('<b>This is my first program </b>');

            }

         //-->

      </script>

         </body>

</html>
 ```
// output: This is my first program
 In above example, if student_age is grater then 10 then statement “This is my first program” will get printed or displayed.

Note: if should be in lowercase letters. Uppercase letters (IF or If) will generate an error.

The else Statement
else statement is used to specify a block of code to be executed if the

expression is false. Following is the syntax of else statement:
```
Syntax

if (expression) {

    block of code is executed if the expression is true

} else { 

    block of code is executed if the expression is false

}
```
In the above syntax, if the expression is true then if condition statement is

get executed, otherwise else condition is executed.

