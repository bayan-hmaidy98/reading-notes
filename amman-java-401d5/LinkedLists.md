## Big O: Analysis of Algorithm Efficiency

Big O is used to describe the efficiency of a witten algorithm regarding 2 aspects: **Running Time** (time required t execute the function) and **Memory Space** (amount of memory  used to store data after execting the function). 

### Anylzing Time and space aspects: 

4 facors affect the running time and memory space factors: 
1. Input size: it doesn't mean the number of parameters, but size of each parameter passed. (n)
2. Units of measurments: for the running time we consider the excecution time of the algorithem regardless powerful state of differnt machines, operations are excuted as number of lines, and basic opation of the algorithmthat runs the most of the time. 
For memory space, the amount of space to hold the code, amount of space to hold the output data and input data (if not passed directly), and amount of space to hold the working space especially the stack space. 
3. Order of growths: 
a. constant complexity growth that is independant on the input size. (1)
b. Logarithmic complexity growth: the rate of complexity is decreased when the value of on n is growing rapidly. (lgn)
c. Linear complexity growth: the size of the input affects it's complexity directly. (n)
d. Linearthmic: mixes the logarthmic and linear complexity. (nlgn)
e. Quadratic complexity growth: the complexity is measured by input sise to the power 2. (n^2)
f. Cubic complexity growth: the complexity is measured by input sise to the power 3. (n^3)
g. Exponential complexity growth: complexity is growing fast regarding the input size. (2^n)
h. Factorial complexity: that the our space and time requirements grow extremely fast, relative to the input size. (n!)

**Worst case:** runs all of the possible values. It's also known as Big O(oh).
**Best case:** runs the quickest for the possible values. Also, it's known as Big Omega. 
**Average case:** runs random number of possible values. Known as Big Theta. 

## Linked lists

Linked lists consists of nodes connected with link. Each node **refere** to next node. 


Notes: 
1. Linked lists are described to be singly or doubly. Both relates to the refernce between node. Singly says there is only one reference which is next and doubly says there are 2 references which are next and previous. 
2. First node of linked list called Head. 
3. The currently node looked at is called current. 
4. Last node has no next, it's null. 
5. for loop can't be used to move between loops. This is Next job. 
6. while loop allows us to check the value of the next node, so that we use it. 
7. To check the values inside the linked list, we use `includes`. 