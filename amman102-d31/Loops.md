# Operators and Loops 

I have already discused the operators earlier in read 04. You can get back to it by clicking here [Operators.](https://bayan-hmaidy98.github.io/reading-notes/JavaScript) 

# Loops 
Loops offer a quick and easy way to do something repeatedly. `You can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another. ` 

The various loop mechanisms offer different ways to determine the start and end points of the loop. There are various situations that are more easily served by one type of loop over the others. For today, we'll talk about **For** and **While**. 

## For loop
A for loop repeats until *a specified condition evaluates to false.* The JavaScript for loop is similar to the Java and C for loop.

A for statement looks as follows:

> for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement

  The process looks like the following:

  1. Our process starts with initailizing the **initial expression** or **expressions** if there are more than one counter.
  2. Then the condition is checked to be true or false. *Note* that if it is false, it will not excute what inside the loop.
  3. Then it will excute the statement or statement inside the **curly brackets**.
4. The increment expression is excuted by then and would be right back to step 2.

## Whlie loop


**A while statement** executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

while (condition)
  statement
If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs **before** statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

To execute multiple statements, use a block statement ({ ... }) to group those statements, as we have mentioned in before loop. 
