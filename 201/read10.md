## Error Handling & Debugging
After Reading this you will determine what 
went wrong in your JavaScript and how to fix it. you will learn about: 
![w](https://res.cloudinary.com/practicaldev/image/fetch/s--Qco4wGFO--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f3meoc4rbh3xft7g8yw9.png)
1. THE CONSOLE & 
DEV TOOLS
2. COMMON 
PROBLEMS 
3. HANDLING 
ERRORS 

### EXECUTION CONTEXT 

Every statement in a script lives in one of three 
execution contexts: 
1.  GLOBAL CONTEXT :Code that is in the script, but not in a function. 
There is only one global context in any page. 

2. FUNCTION CONTEXT: Code that is being run within a function. 
Each function has its own function context.
3. EVAL CONTEXT (NOT SHOWN) :Text is executed like code in an internal function 

### VARIABLE SCOPE
1. GLOBAL SCOP
2. FUNCTION-LEVEL SCOPE
### EXECUTION CONTEXT & HOISTING
Each time a script enters a new execution context, there are two phases 
of activity
1. PREPARE
* The new scope is created 
* Variables, functions, and arguments are created 
* The value of the this keyword is determined 
2. EXECUTE 
* Now it can assign values to variables 
* Reference functions and run their code 
* Execute statements

### COMMON ERRORS
![w](https://cdn-images-1.medium.com/max/640/1*zFv75wl_zI21KdPf9IgrJQ.jpeg)
Here is a list of common errors you might find 
with your scripts. 
1. GO BACK TO BASICS : GO BACK TO BASICS
2. MISSED/ EXTRA 
CHARACTERS :MISSED/ EXTRA 
CHARACTERS
3. DATA TYPE ISSUES: Using= rather than == will assign 
a value to a variable, not check 
that the values match.


#### If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements.Use them to give your users helpful feedback.