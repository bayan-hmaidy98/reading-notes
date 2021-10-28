## Trees

Trees are just one more type of **data structure.** Here is some related terms to trees: 
1. Node: elemnt holds value and reference. 
2. Root: begining of the tree. 
3. K: maximum number ofchildren can any node **have**. Each type has a special numbe, for example: binary trees has 2 children. Children can be refered in binar trees using **Left** to refer to one child and **Right** to refer to the other one. 
4. Edge: **link** between child and parent. 
5. Height: number of children or nodes or links from the begining (root) to the end (leaf). 

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

All of the above terms are established to seek **Traversing**. Traversing is important for searching, printing special data or maybe changing values!

### Depth First

A way of traversing to go through the nodes or height of tree. There are three types of depth: pre-order, in-order, post-order.


**Breedth First** related to traverse between  node: node-by-node. It uses *queue*. 


### Binary Tree Vs K-ary Trees
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree2.PNG)

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each Node is able to have.