## Graphs

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

Here is some common terminology used when working with Graphs:

* Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
* Edge - An edge is a connection between two nodes.
* Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
* Degree - The degree of a vertex is the number of edges connected to that vertex.

## Directed vs Undirected

## Undirected Graphs
An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

![gr](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)


## Directed Graphs (Digraph)

A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.
![gr](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)


## Complete  vs Connected vs Disconnected

1. A complete graph is when all nodes are connected to all other nodes.

2. A connected graph is graph that has all of vertices/nodes have at least one edge.

3. A disconnected graph is a graph where some vertices may not have edges.

## Acyclic vs Cyclic

* An acyclic graph is a directed graph without cycles.

* A cycle is when a node can be traversed through and potentially end up back at itself.

## Graph Representation

We represent graphs through:

1. Adjacency Matrix
2. Adjacency List

## Traversals

1. Breadth First

you start at a specific vertex/node. This node must be specified when call the BreadthFirst() method.
The breadth-first traversal of a graph is similar to that of a tree, except graphs can have cycles and cause infinite loops.
Keep track of the vertices/nodes that have been visited.


2. Depth First

Use a stack for a depth first search.
Push the root node into the stack
Start a while loop while the stack is not empty
Peek at the top node in the stack
If top node has unvisited children, mark the top node as visited, and then push any unvisited children back into the stack
If top nodes does not have any unvisited children, Pop that node off the stack.
repeat until the stack is empty.

## Real World Uses of Graphs
Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:

1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of products