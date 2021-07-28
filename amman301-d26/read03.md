# Lists and Keys 

It's common to render lists inside the componenets. To do that, we should provide the list item with a key or a warning would appear while running the code. 

### What is the key?

> A “key” is a special string attribute you need to include when creating lists of elements. If it wasn't provided, the index would be taken as a key. Keys help React identify which items have changed, are added, or are removed.

Note that, It's not recommended to use index, because the order of item may change and cause a mess in the code. 

**The best practice** is to add the key inside the `<ul>` instead of `<li>`.

**Finally,** keys must be unique among siblings but it's ok to use the same keys in different arrays. `They don’t need to be globally unique.` 

# How to use the spread operator in JS


` In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments. `

## Tasks can be done using `...`
1. Copying an array
2. Concatenating or combining arrays
3. Using Math functions
3. Using an array as arguments
4. Adding an item to a list
**5. Adding to state in React**
6. Combining objects
7. Converting NodeList to an array

**Examples** for each case are provided in the [Link.](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

*Spread operator* is not supportes in internet explorer and on older mobile devices.


# How to pass functions between components?

Create the dunction **beneath** the value is changed.

We do this because the functions that control one components state have to reside in the same component as the state. So, if one component needs to update the state of another then it needs to have the function from the first component.

