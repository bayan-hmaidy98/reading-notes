## Java Primitives versus Objects

Since Java has 2 types of variables: reference and primitive, we need to distinguish between them and know when to use each. 

### Primitive variables 

1. They live in the stack in the memory, so they are accessed faster. 
2. They occupy less space in the memory. 
3. The perform faster in Java code than reference variables. 
4. They are initiallized to default values when not declaring them directly: 0 for numeris, false for boolean, \u0000 for char.
5. They are not allowed to be used in the parameterized type.

### Refernce variables

1. They live in the heap of the stack memory, they are slower to access.
2. They occupy more space in the memory. 
3. They are slower in performance than primitive variables.
4.They are initialized to the default value null if not initiallized manually. 
5. They are allowed to be used in the parameterized type.

## Exception

Eception is an event occured when there is error and it braks the normal flow of the code. 

### List of possible methods from stack to handle the error when occured: 
1. Method call from main 
2. Method call with an eception handler
3. Method call without an eception handler
4. Method call where error occured 

In java, code might throw exception throw **Catch or Specify Requirments** 

### Types of exception

1. Checked exception: when the program is well-written, it will catch the eception to notify the user about **mistakes**.

2. Erorr: this one is external to the application. The appliction doesn't always choose to catch this kind of exceptions. 

3. Runtime exception: it's internal to the application, and as a result **the application usually cannot anticipate or recover from.**
