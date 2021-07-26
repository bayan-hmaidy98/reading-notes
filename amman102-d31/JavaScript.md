
# Expressions & Operators used in JavaScript
There are so many Operators that are used in JS, we'll discuss some of them below:

* Assignment operators
* Comparison operators
* Arithmetic operators
* Bitwise operators
* Logical operators
* String operators
* Conditional (ternary) operator
* Comma operator
* Unary operators
* Relational operators

An **Assignment operator** assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = y assigns the value of y to x. *Like most expressions, assignments like x = y have a return value.*

When chaining these expressions, each assignment is evaluated right-to-left. Consider these examples:

`w = z = x = y is equivalent to w = (z = (x = y)) or x = y; z = y; w = y
z += x *= y is equivalent to z += (x *= y) or tmp = x * y; x *= y; z += tmp (except without the tmp).`

## Destructuring
The **destructuring assignment syntax** is a JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that *mirrors* the construction of array and object literals.

An **Arithmetic operators** takes numerical values (either literals or variables) as their operands and returns a single numerical value. The standard arithmetic operators are addition (+), subtraction (-), multiplication (*), and division (/). These operators work as they do in most other programming languages when used with floating point numbers (in particular, note that division by zero produces Infinity)

A **comparison operator** compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. `Here we can benifit from " == " command.`

## Bitwise Shift Operators

A **bitwise operator** treats their operands as a set of 32 bits (zeros and ones), rather than as decimal, hexadecimal, or octal numbers. Bitwise operators perform their operations on such binary representations, *but they return standard JavaScript numerical values.* **The bitwise shift** operators take two operands: the first is a quantity to be shifted, and the second specifies the number of bit positions by which the first operand is to be shifted. The direction of the shift operation is controlled by the operator used.

**Logical operators** are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. The logical operators are described in the following table.

As **logical expressions** are evaluated left to right, they are tested for possible "short-circuit" evaluation using the following rules:

* False && anything is short-circuit evaluated to false.
* True || anything is short-circuit evaluated to true.

*Note that the anything part of the above expressions is not evaluated, so any side effects of doing so do not take effect.*

In addition to the **comparison operators**, which can be used on string values, the concatenation operator (+) **concatenates** two string values together, returning another string that is the union of the two operand strings.

The **conditional operator** is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition. A **unary operation** is an operation with only one operand.

The **comma operator** (,) evaluates both of its operands and returns the value of the last operand. This operator is primarily used inside a for loop, to allow multiple variables to be updated each time through the loop. It is regarded bad style to use it elsewhere, when it is not necessary. Often two separate statements can and should be used instead.

A **relational operator** compares its operands and returns a Boolean value based on whether the comparison is true.

## Control Flow

The **control flow** is the order in which the computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. Control flow means that when you read a script, you must not only read from start to finish but also look at **program structure and how it affects order of execution.**

