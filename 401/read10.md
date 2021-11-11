# What is a Stack
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

## Common terminology for a stack is

1- Push - Nodes or items that are put into the stack are pushed
2- Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
3- Top - This is the top of the stack.
4- peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
5- IsEmpty - returns true when stack is empty otherwise returns false.

## Stacks follow these concepts:

FILO
First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

LIFO
Last In First Out

![stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

## There are two types of operations in Stack-
1- Push– To add data into the stack.
2- Pop– To remove data from the stack.

## How can we implement a stack in Python?
In Python, we can implement python stacks by:
1- Using the built-in List data structure. Python’s built-in List data structure comes with methods to simulate both and operations.
2- Using the deque library which efficiently provides stack and queue operations in one object.
As mentioned earlier, we can add items to a stack using the “PUSH” operation and remove items using the “POP” operation.

### PUSH Operation
![push](https://miro.medium.com/max/375/0*GnkZ7osmTHzpyyKl.png)

### POP Operation
![pop](https://miro.medium.com/max/339/1*CplTWJmg9oAufHngc_JNpw.png)

## The collections.deque Class
Because deques support adding and removing elements from both ends equally well, they can serve both as queues and as stacks.
collections.deque is a favorable choice if you’re looking for a stack data structure in Python’s standard library with the performance characteristics of a linked-list implementation.