# Layouts 

## What are the types of boxes on HTML?

### 1. Block-level box.
Bolck boxes **start** new line in their apperance. Examples: `<h1>` `<p>` `<ul>` `<li>`

### 2. Inline box.
Inline box **floats** through the text itself. Examples: `<img>` `<b>` `<i>`.

### Parent  element 
We call a block-level element inside another block-level element a parent element. It's popular to group many elements in `<div>`  and it's called ** containing element**


## Position of elements 
It relates to the layout of the page (normal, relative, and absolute). It's specified using **position** property in css. 

### 1. Normal flow: 
It starts on a new line always and doesn't accept another element in the same line.

### 2. Relative 
It moves the element to the specified orientation from the position it would be in **normal flow.** 

### 3. Absolute
It relates in its position to the containing element. It does not affect the position of any surrounding elements.

## Normal flow (again!)
1. Static: the defualt property of html, and we use it when a containing element (as a whole) is set to be different position and want to specify one of it's elemnts to be `static`. 

2. Relative: It moves an element in relation to where it would have been in normal flow. It does not affect the position of any surrounding elements.

3. Absolute: In this case, the box is taken out of normal flow and no longer affects the position of other elements on the page. 

4. fixed: t positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place.

#### Z-index 
If you want to control which element sits on top, you can use the z-index property. Its value 
is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10
will appear over the top of one with a z-index of 5. 

#### Float 
The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible. Anything else that sits inside the containing element will **flow around the element** that is floated.

#### Clear
The clear property allows you to say that no element (within the same containing element) 
should touch the left or right-hand sides of a box. 

##### Margin
This creates a gap between the columns.

#### Screen Sizes
Since the website is visited by users from different devices sizes', the design must fit all the screen sizes. 