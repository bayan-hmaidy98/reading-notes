# Node JS - Modules and require()

Devlopers **Do not** write all the code in one file, because: 
1. It would be really hard to manage.
2. Other developers can't refactor or extend components into it.

### How is this issue solved? 
By splitting the code into logical modules, each module has a specified purpose or functionality. These modules are called when they are needed.

**Note:** A module is just a *JS* file.

### After creating modules, how can we call/use them in other modules to be used?

We use the require 

# Functional programming

### What is functional programming?

`Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.`

### What is a pure function and how do we know if something is a pure function?

Pure functions are the functions that return the same result if given the same arguments (it is also referred as deterministic). ALso, it does not cause any observable side effects

### What are the benefits of a pure function?

The code’s definitely easier to **test**.

### What is immutability?

Unchanging over time or unable to be changed. Its state cannot change after it’s created.

### What is Referential transparency?

`pure functions + immutable data = referential transparency`
