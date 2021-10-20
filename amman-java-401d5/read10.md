
## Stack and Queues

### Stack
When dealing with stack, the following terms are used: 

Push: add new value to the stack
Pop: remove value from stack 
Peek: refere to the **top** of the stack
IsEmpty: check wether the stack is empty or not. 

Push illustration: 
![push](https://www.tutorialspoint.com/data_structures_algorithms/images/stack_push_operation.jpg)

When new node is added, it's next refers to the top, top refers to the new node. 

Pop illustration: 
![pop](https://lh3.googleusercontent.com/proxy/2dr8ax2X57NQZVxNwSrfcgvh4b4gQ64Ak21Mx5R-LNAycs-MixMltvgbbdl7u97vguEdxPR0TowGBYWpF0dff6GqqB0irxm0er8ptV4QGBkh5MT6nanBPhv3XRJnVHTRRSUioau8u0uSpdCt88GQ)

When removing a node, create a temporary node to point to the top, make the top is the next node, remove the next of the temporary and return its value. 


Peek can be returned by getting the value of the top but we need to make sure that the stack is not empty using isEmpty().

### Queue

When dealing with queue, the following terms are used: 

Enqueue: add new value to the queue
Dequeue: remove value from queue
Peek: refere to the **front** of the queue
IsEmpty: check wether the queue is empty or not. 

Enqueue illustration: 
![Enqueue](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQvvBamtmLTHELsxf0M2_N52grgFJK7gDWNg&usqp=CAU)

When enqueue the queue, a new node is created, next value of the rear is assigned to the new node and rear is moved to the next value

Dequeue illustration: 

![Dequeue](https://www.tutorialspoint.com/data_structures_algorithms/images/queue_dequeue_diagram.jpg)

When dequeue the queue, a temporary reference is created and points to the front, front is assigned to its next, the temporary now is eliminated by removing the reference, and the value of the temporary is returned. 

Peek can be returned by getting the value of the front but we need to make sure that the queue is not empty using isEmpty().
