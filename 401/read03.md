# FileIO & Exceptions


## Opening and Closing a File in Python

When you want to work with a file, the first thing to do is to open it

```
file = open('dog_breeds.txt')
```
After you open a file, the next thing to learn is how to close it.

```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```
or by using this way 

```
with open('dog_breeds.txt') as reader:
    # Further file processing goes here
 ``` 

The with statement automatically takes care of closing the file once it leaves the with block, even in cases of error. I highly recommend that you use the with statement as much as possible, as it allows for cleaner code and makes handling any unexpected errors easier for you.

Most likely, you’ll also want to use the second positional argument, mode. This argument is a string that contains multiple characters to represent how you want to open the file. The default and most common is 'r', which represents opening the file in read-only mode as a text file:
```
with open('dog_breeds.txt', 'r') as reader:
    # Further file processing goes here
with open('dog_breeds.txt', 'r') as reader:
    # Further file processing goes here

```
```
Character	Meaning
'r'	Open for reading (default)
'w'	Open for writing, truncating (overwriting) the file first
'rb' or 'wb'	Open in binary mode (read/write using byte data)

```
## Reading Opened Files
Once you’ve opened up a file, you’ll want to read or write to the file. First off, let’s cover reading a file. There are multiple methods that can be called on a file object to help you out:


Method	What It Does
* .read(size=-1)	This reads from the file based on the number of size bytes. If no argument is passed or None or -1 is passed, then the entire file is read.

* .readline(size=-1)	This reads at most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or rest of the line) is read.
* .readlines()	This reads the remaining lines from the file object and returns them as a list.

## Writing Opened Files

Method	What It Does
* .write(string)	This writes the string to the file.
* .writelines(seq)	This writes the sequence to the file. o line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

```
with open('dog_breeds.txt', 'r') as reader:
    # Note: readlines doesn't trim the line endings
    dog_breeds = reader.readlines()

with open('dog_breeds_reversed.txt', 'w') as writer:
    # Alternatively you could use
    # writer.writelines(reversed(dog_breeds))

    # Write the dog breeds to the file in reversed order
    for breed in reversed(dog_breeds):
        writer.write(breed)
```

## Iterating Over Each Line in the File
```
with open('dog_breeds.txt', 'r') as reader:
>>>     for line in reader.readlines():
>>>         print(line, end='')
```



# Exceptions in Python
## syntax errors and exceptions,

Errors are the problems in a program due to which the program will stop the execution. On the other hand, exceptions are raised when some internal events occur which changes the normal flow of the program. 
Two types of Error occurs in python. 

1- Syntax errors

2- Logical errors (Exceptions) 


 
```
Exception	Description
IndexError	When the wrong index of a list is retrieved.
AssertionError	It occurs when the assert statement fails
AttributeError	It occurs when an attribute assignment is failed.
ImportError	It occurs when an imported module is not found.
KeyError	It occurs when the key of the dictionary is not found.
NameError	It occurs when the variable is not defined.
MemoryError	It occurs when a program runs out of memory.
TypeError	It occurs when a function and operation are applied in an incorrect type.
```

### Error Handling
```

# put unsafe operation in try block
try:
     print("code start")
          
     # unsafe operation perform
     print(1 / 0)
  
# if error occur the it goes in except block
except:
     print("an error occurs")
  
# final code in finally block
finally:
     print("GeeksForGeeks")
```


After seeing the difference between syntax errors and exceptions, you learned about various ways to raise, catch, and handle exceptions in Python. In this article, you saw the following options:

* raise allows you to throw an exception at any time.
* assert enables you to verify if a certain condition is met and throw an exception if it isn’t.
* In the try clause, all statements are executed until an exception is encountered.
* except is used to catch and handle the exception(s) that are encountered in the try clause.
* else lets you code sections that should run only when no exceptions are encountered in the try clause.
* finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.