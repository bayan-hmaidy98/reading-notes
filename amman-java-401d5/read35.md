# Graphs

A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes also referred to as vertices and the edges are lines that connect any two nodes in the graph.

## Undirected Graphs

From it's defintion, we can say that it's not directed to any direction. Here's an example: 

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

The graph has **6** nodes and **7** edges. 

## Directed Graphs

Here we have directions in edges, each node can be directed to another node through the directed edges. See the imagebelow: 

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

Here also the The graph has **6** nodes but **8** edges. 

### Complete vs Connected vs Disconnected

Complete: *All nodes* are connected to each others. 
Connected: Each node is connected to at least one node. Each node has at least one edge.
Disconnected: Some nodes may be not connected to others. 

### Acyclic vs Cyclic

To understand the acyclic, let's see what exactly cyclic means. Cyclic simply means a node started directing to other node and ended up redirected at too. This is not the case in acyclic. They are both directed graphs. 

## Graph Representation

1. Adjacency matrix

In matrix, we have columns and rows, when we have a position of row, column index, this is a node or vertex. The values inside the matrix represent the edges between the vertecies. 

2. Adjacency  list 

It's easied to implement the graphs using adjacency method. `An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.`


### Weighted Graphs

Weighted graphs mean that each edge has weight.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)

 This is how would it look like in adjacency matrix and adjacency list respectivly: 

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightMatrix.PNG)

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightList.PNG)

