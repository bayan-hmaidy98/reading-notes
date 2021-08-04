# Understanding the JavaScript Call Stack

### What is a ‘call’?

The **call stack** is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

### How many ‘calls’ can happen at once?

Two calls.

### What does LIFO mean?
First In, Last Out. It means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

### What causes a Stack Overflow?

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

# JavaScript error messages

### What is a ‘refrence error’?

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

### What is a ‘syntax error’?
Syntax error occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

### What is a ‘range error’?

A RangeError is thrown when trying to pass a number as an argument to a function that does not allow a range that includes that number.

### What is a ‘type error’?

Types of errors show up when the types 
(number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

### What is a breakpoint?

A breakpoint is an intentional stopping or pausing place in a program, put in place for debugging purposes. It is also sometimes simply referred to as a pause. More generally, a breakpoint is a means of acquiring knowledge about a program during its execution.
