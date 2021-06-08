# Transformers 
The tranform property have 2 settings: 2-d and 3-d. Through the illustration, some of their properties will be presented. **Note** that the browsers don't support tansform that much! So, in tranform syntax, `the value specifies the transform type followed by a specific amount inside parentheses,` and `the un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.`

## Rotate 
Rotate supports 2-d and 3-d. It provides the ability to rotate an element from 0 to 360 degrees. **Note** that it rotates around the specified axis. If the axis is not mentioned, the point of rotation is set to default at the center of the element (50% 50%, both horizontally and vertically).

## Scale 
Scale supports 2-d and 3-d. `It allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.` You can specify to scale the height, width, or both. 

## Translate 
Translate supports 2-d and 3-d. It `works a bit like that of relative positioning, pushing and pulling an element in different directions **without** interrupting the normal flow of the document. +ve values tend to push the element **down and to the right** of the *default* position, and -ve values tend  to push the element **up and to the left** of the *default* position. 

## Skew 
It works **only** for 2-d. `It is used to distort elements on the horizontal axis, vertical axis, or both.` Skew is measured in degrees, like **rotate**.

### Combining transform
All of the above propertied could be comined togather in one decleration, for example:
> transform: skew(10deg, 20deg) translateX(20px) rotate(25deg) scale(.75);

## Perspective 
Perspective means the place you stand in to see the 3-d element. You can set the perspective in css in 2 ways: `one way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed.`


# Transitions and Animations

## Transition
In order to apply transitions for a state, change must occur. For example, the following pseudo-classes: `:hover, :focus, :active, and :target`

### Vendor prefix 
Vendor prefixes are used for **the best support across all browsers.** 
**Note** that in transitional property, `only the properties identified within the transition-property value will be affected by any transitions.` And keep in mind, **not all the properities may be transioned,** nly properties that have an identifiable halfway point. 

## Transition timing
It determine the spped of the transition and have different values like: Linear, ease-in, and ease-out. `Linear specifies a constant speed from one state to another. The ease-in value identifies a transition that starts slowly and speeds up throughout the transition, while the ease-out value identifies a transition that starts quickly and slows down throughout the transition. The ease-in-out value identifies a transition that starts slowly, speeds up in the middle, then slows down again before ending.`. A **time delay** can be sit to delay the transition property and then it starts to function as required in the soecified **timing function.**

**Lucky us!** All of the above properties have a **shorthand property transition** that supports it's values beside their properties.

## Animations 

To set any element to animation properties, `@keyframes` rule must be provied at the begining. `The different keyframe breakpoints are set using percentages, starting at 0% and working to 100% with an intermediate breakpoint at 50%.` **Note** that when you declare an animation, it must be assigned to an element using `animation-name`. Also, like transition, animation had duration, timming function and delay. 

### Animation iteration & direction 

To have repeated repeated animation, we use the property `animation-iteration-count`. It could have an `integer` value or `infinite` keyword. Also, you can set the direction of the animation: ormal, reverse, alternate, and alternate-reverse. 





