# Python Scope
A variable is only available from inside the region it is created. This is called scope.

## Local Scope
A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.
```
def myfunc():
  x = 300
  print(x)

myfunc()

```
## Modules: The Global Scope
From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. The namespace of this module is the main global scope of your program.

Note: In Python, the notions of global scope and global names are tightly associated with module files. For example, if you define a name at the top level of any Python module, then that name is considered global to the module. That’s the reason why this kind of scope is also called module scope.

If you’re working in a Python interactive session, then you’ll notice that '__main__' is also the name of its main module. To check that out, open an interactive session and type in the following:

```
>>> __name__
'__main__'
```

## Global Keyword
If you need to create a global variable, but are stuck in the local scope, you can use the global keyword.

The global keyword makes the variable global.

```
def myfunc():
  global x
  x = 300

myfunc()

print(x)
```

also, use the global keyword if you want to make a change to a global variable inside a function.

Example
To change the value of a global variable inside a function, refer to the variable by using the global keyword:
```
x = 300

def myfunc():
  global x
  x = 200

myfunc()

print(x)
```

## The nonlocal Statement
Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope. The following example shows how you can use nonlocal to modify a variable defined in the enclosing or nonlocal scope:

## Conclusion
The scope of a variable or name defines its visibility throughout your code. In Python, scope is implemented as either a Local, Enclosing, Global, or Built-in scope. When you use a variable or name, Python searches these scopes sequentially to resolve it. If the name isn’t found, then you’ll get an error. This is the general mechanism that Python uses for name resolution and is known as the LEGB rule.

You’re now able to:

Take advantage of Python scope to avoid or minimize bugs related to name collision
Make good use of global and local names across your programs to improve code maintainability
Use a coherent strategy to access, modify, or update names across all your Python code