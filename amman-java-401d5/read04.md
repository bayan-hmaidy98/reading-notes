## Object-Oriented Programming Concepts

### Objects 

Objects in programming are created to **simulate** *real-world objects*. This is done by realising what makes real-world object a real-worl object! In other words, all real- world objects share 2 charecteristics that make them ditinguished from any other objects, **state** & **behaviour**. Objects in programming share another property with real objects, they have objects inside other objects. 

So, let's dig deeper in states and behaviours: 
States are stored in object's field. Behaviours or **methods** uses internal **states** for their operations to get the states updated. Also, states and behaviours obtain their own rules in order to work in the expected way.

### Benefits of using objects in coding: 
1. Creating any object will not affect any other objects. They work independantly. 
2. Data encapsulation, since `details of its internal implementation remain hidden from the outside world.` 
3. Code can be reused. 
4. Pluggability and debugging are easier since objects can be replaced if there is something wron with their building. 

### Classes 

Classes can be defined as `the blueprint from which individual objects are created.` In this way, we can have many instances to create using **class** of **objects.** 

In classes, come sub classes can **inherit** all the fields and methods from the class. This subclass, can add  then other fields and methods that won't **affect** the class. 

### Declaring a class 

The syntax is as following: 

`class MyClass {
    // field, constructor, and 
    // method declarations
}`

We have mentioned earlier what are fields and methods. In order to make new instance (initializtion) we use constructors. If it was a subclass, we declare it as the following: 

`class MyClass extends MySuperClass implements YourInterface {
    // field, constructor, and
    // method declarations
}`

Extends mean it can use the fields, constructor, and methods in the class (using the keyword super). Public and private determine which classes can access the subclass. 

Notes: 
1. As you know, class name starts with an uppercase.
2. `Java does not support multiple inheritance.` This means that a subclass has only **one parent**. 
3. Class can implement many interfaces. 

## Declaring Member Variables

Member variables are the same as fields. The syntax of declaring the member values are: 
`modifier fild's type field's name`

### Access modifier 

Access modifiers are used to `control what other classes have access to a member field.` 
Till now, we were intorduced for 2 types of access modifiers: private and public. Sometimes, fields are modified to be private in order to be only used from object itself. On the other hand, fields can be accessed indirectly from if the methods are added as **public** method. 

**Note:** The first word in methods is common to be a verb.

## Defining methods 

To define a method, six components must be used in the order provided below:

1. Modifiers
2. Return type
3. Method name
4. Parameter List included in paranthesis
5. Exceptopn list
6. Method body

**Important Note:** `Typically, a method has a unique name within its class. However, a method might have the same name as other methods due to method overloading.` It is re;ated to the method signatures. Also related to super class and sub class.

Back to the note above, in overloading, you can't have the same signature for 2 or more methods even if they return different types. 

## Providing constructors for your classes

To declare a constuctor, you can follow the steps in declaring methods except constructors don't have a return type and they use class name. Also, a class can have more than one constructor. Bare in mind, you can't have the same argument for more than one constructor. 

## Passing information to a method or a constructor

There are cases you can't define hoe many arguments you are going to use in the method. Varargs is used in this case and even if there is np argument to pass. 

`(typeOfLastParameter... parameterName)` 

Notes: 
1. In naming the parameters, they must be unique in their scope.
2. Parameters can have the same name as one in the parameters field. This would make the code shadowed (harder to read).

## Binary, Decimal and Hexadecimal Numbers


| ----------- | Decimal Numbers      | Binary Numbers | Hexadecimal Numbers |
| ----------- | ----------- | ----------- | ----------- |
| Base      | 10      | 2       |16       |
| Symbols      | 0,1,2,3,4,5,6,7,8,9      | 0,1       |0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F       |

Note: `Count up until just before the "Base Number", then start at 0 again, but first you add 1 to the number on your left.` let's review it to the upper number systems: 

Decimal: 0,1,2,...,9,10

Binary: 0,1,10,11,.. 

HexaDeciaml: 0,1,2,..,9,A,B,..,F,10