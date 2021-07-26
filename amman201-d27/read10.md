# Execution context

Execution context (EC) is defined as the environment in which the JavaScript code is executed. Every statement in a script lives in one of three execution contexts: 
1. Global execution
2. Function execution
3. Eval execution
**Note** that the first two execution contexts correspond with the notion of scope: global scope and local (function-level) scope. 

## The stack
The Js interpreter processes one line of code at a time. When a statement needs data from another function, it **stacks** the new function of the current task.

# Errors

Error objects can help you find where your mistakes are 
and browsers have tools to help you read them. They contain the following properties:
Name, message, file number, and line number. 

## Errors types

### * Syntax Error
### * Reference error
### * Eval error
### * URI error
### * Type error
### * Range error 

**NaN** is not an error type, it is a sign that notifys that you're using a value that is not a number. 

## Dealing with errors

In order to deal with errors and eleminate them from the code, here are 2 things to manage fixing errors

### 1. Debug the script to fix errors
### 2. Handle errors gracefully

You need to determine 2 things while dealing with errors: where is th error and what exactly the problem. 