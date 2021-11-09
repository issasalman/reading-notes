# List comprehension

Python provides several methods for creating lists. The list comprehension feature is one of the most effective of these methods. It allows you to create lists with just one line of code.


It can be used to create new lists from other iterable elements such as arrays, strings, tuples, lists, and so on. It consists of brackets containing the expression. To iterate over all of the elements, the system uses the for loop to execute the expression for each one.

The following is the Python syntax:
```
our_new_list = [expression for element in our_old_list if condition]
```
Example 1:

We’ll make a simple list using Python comprehension in this example:
```
Input:
 a = [i for i in range(8)]
 print a
Output:
 [0, 1, 2, 3, 4,5,6,7]
 ```

 Example 2:

List comprehension isn’t just for integers; it can also be applied to strings. In this example, we will use list comprehension to create a list of the first letter of every word in our original list
```
Input: 
 my_list = [“playing”, “is”, “fun”]
 result = [word[0] for word in my_list]
 print result
Output
[‘p’, ‘i’, ‘f’]
```

## Difference between list comprehension and for loop
The for loop is a common way to iterate through a list. List comprehension, on the other hand, is a more efficient way to iterate through a list because it requires fewer lines of code.

Here is an example to illustrate the difference. We will start with an empty list and modify it to make it a list of even numbers:

### using for loop
```
Input
# creating the empty list
 old_list = []
 # we will use the for loop to create the new list
 for x in range(10):
 old_list.append(x*2)
 print old_list 
Output: 
 [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
 ```
 ### using list comprehension
```
 Input: 
 # creating the set with the help of list comprehension
 old_list = [x*2 for x in range(10)]
 print old_list
Output:
 [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
 ```

 # Decorators in Python

 A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure. Decorators are usually called before the definition of a function you want to decorate. 
```
 def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper
```

### without using decorator
```
def say_hi():
    return 'hello there'

decorate = uppercase_decorator(say_hi)
decorate()
```
### with  decorator
```
@uppercase_decorator
def say_hi():
    return 'hello there'
```
