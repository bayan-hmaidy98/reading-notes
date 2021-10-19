## OO Design

### Rules to follow in programming

DON'T REPEAT YOURSELF (DRY)

is a principle aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization.

Repetition in code is a waste in **time, performance and space**; that's why we need to keep it as simple as possible.

The principle was formulated by Andy Hunt and Dave Thomas who applied it to include databases schemas, test plans, documentation and more.

When applied successfully, modification of any element within the system shouldn't require any modifications for logically unrelated elements.

### Why do we need an MVP in software development ?

Be able to test a product hypothesis with minimal resources.

Accelerate learning.

Reduce wasted engineering hours.

Get the product to early customers as soon as possible.

Base for other products.

### SOLID principles in real life

* S - single responsibility principle - class or module should have only one reason to change

Real life example - the "duck" vehicle are street legal and water-capable, and they only change from driving on land to going out on the water, and from being driven in the water to land.
* O - open/closed principle - a class that does what it needs to flawlessly and does not need to be changed later, but can be extended.

Real life example - a smart phone that doesn't need to be changed itself, but you can add apps on the phone.
* L - liskov substitution principle - any child type of a parent type should be able to stand in for that parent

Real life example - Cooking stew with various ingredients in the stew, while asking if the ingredients are edible or not.
* I - interface segregation principle - don't want to force clients to depend on things they don't actually need

Real life example - The soup of the day on a menu at a restuarant. The reason why it only says soup of the day is because it changes everyday.
* D - dependency inversion - depends upon abstractions rather than upon concrete details

Real life example - Using a credit card to pay groceries with, and the clerk swiping your credit card with a visa machine.
