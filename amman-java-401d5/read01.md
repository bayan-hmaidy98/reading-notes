# Java Basics 

## Language Basics: 

### Variables:

Fields in Java refers to variables and vice versa. Java defines 4 types of variables: 

1. Non-static fields or instance variables: they are declared without the keyword 'static'. 

2. Class variables or static fields: they are declared with the keyword 'static'. It means that there is only one copy of the variable, though it could be initiallized many times. 

3. Local variables: It's used to store the temprory values. The term 'Local' determine where the variable was declared. 

4. Parameters: they are the parameters passed through classes. Note that they are called **variables** not **fields**. 

### Naming:

Rules you need to follow in naming varibles:
 
`1. Variable names are case-sensitive. A variable's name can be any legal identifier — an unlimited-length sequence of Unicode letters and digits, beginning with a letter, the dollar sign "$", or the underscore character "_". The convention, however, is to always begin your variable names with a letter, not "$" or "_". Additionally, the dollar sign character, by convention, is never used at all. You may find some situations where auto-generated names will contain the dollar sign, but your variable names should always avoid using it. A similar convention exists for the underscore character; while it's technically legal to begin your variable's name with "_", this practice is discouraged. White space is not permitted.`

`2. Subsequent characters may be letters, digits, dollar signs, or underscore characters. Conventions (and common sense) apply to this rule as well. When choosing a name for your variables, use full words instead of cryptic abbreviations. Doing so will make your code easier to read and understand. In many cases it will also make your code self-documenting; fields named cadence, speed, and gear, for example, are much more intuitive than abbreviated versions, such as s, c, and g. Also keep in mind that the name you choose must not be a keyword or reserved word.`

`3. If the name you choose consists of only one word, spell that word in all lowercase letters. If it consists of more than one word, capitalize the first letter of each subsequent word. The names gearRatio and currentGear are prime examples of this convention. If your variable stores a constant value, such as static final int NUM_GEARS = 6, the convention changes slightly, capitalizing every letter and separating subsequent words with the underscore character. By convention, the underscore character is never used elsewhere.`

### Operators

Operators are used with one, two, or tree operands. They return a boolean. They also have a precedence which is in following table. 

![Table](/img/Precedence-and-Associativity-of-Operators-in-Java-6.png)


## Expressions, Statements, and Blocks

### Expressions

In expressions, variables, operators, and method invocations are gathered to have a single value. Data type of the value returned by the expression is relatable to ehemnt in the expression. 

### Statements

It's more likely to sentences in the natural languages, but ended by semicolon (;). 

### Blocks

A group or zero of sentences wrapped by braces. 

## Control Flow Statements

In general, code is excuted in the program from the top to the bottom. Sometimes, it won't work like this, according to loops, condionals, and branching. 

## Compiling

Compiling is all about converting the code from high language level to machine language (0,1) to be excuted. 