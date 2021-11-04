# Linked Lists

## What is a Linked List
A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

There are two types of Linked List 

 -1 Singly 2- Doubly.

  We will be implementing a Singly Linked List in this implementation.


  
A linked list must provide the following operations:
* Add nodes
* Remove nodes
* Iterate among nodes
* Find nodes

![LL](https://csharpcorner-mindcrackerinc.netdna-ssl.com/UploadFile/78607b/overview-of-linked-list/Images/Linked%20List.jpg)




  
1- Linked List - A data structure that contains nodes that links/points to the next node in the list.

2- Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.


3- Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

4- Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

5- Next - Each node contains a property called Next. This property contains the reference to the next node.

6- Head - The Head is a reference of type Node to the first node in a linked list.

7- Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

![LL](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)



## Big O

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

* Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

* Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.

If you do a little bit of research on Big O Notation, you’ll quickly find that there are a ton of different equations used to define the space and time complexity of an algorithm, and most of them involve an O (referred to as just “O” or sometimes as “order”), and a variable n, where n is the size of the input (think back to our our ten, thousands, or millions of numbers).
As far as linked lists go, however, the two types of Big O equations to remember are O(1) and O(n).


In order to analyze  limiting factors, we should consider 4 Key Areas for analysis:

* Input Size
* Units of Measurement
* Orders of Growth
* Best Case, Worst Case, and Average Case
![bigo](https://miro.medium.com/max/625/1*FC0XX0-9Vx7yCS0dTS2Zrw.jpeg)

## Differences between array and linked list
![LL](https://miro.medium.com/max/875/1*cUehR5S18XSoVLaPNfNzlA.jpeg)