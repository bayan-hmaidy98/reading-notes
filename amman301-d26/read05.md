# React Docs - thinking in React

### What is the single responsibility principle and how does it apply to components?
It means each compnent should deal **only** with one thing. If the component keeps **growing**, `it should be decomposed into smaller subcomponents.`

### How would you break a mock into a component heirarchy? 
It's about the **refernce**. Things are connected as parent and child, and even growing components should decomposed to subcomponents.

### What does it mean to build a ‘static’ version of your application?

It is reated to interactivity. More thinking, less reading. It means 'to build components that reuse other components and pass data using props. props are a way of passing data from parent to child.` 

### Once you have a static application, what do you need to add?

Now, since we have a staticc version of the app, the only component we have is `render()`, and whenever changes are made, `ReactDOM.render()` can be called again. 

### What are the three questions you can ask to determine if something is state?

**Note:** It is reaaly important to think of the minimal set of mutable state that your app needs.

> 1. Is it passed in from a parent via props? If so, it probably isn’t state.
2. Does it remain unchanged over time? If so, it probably isn’t state.
3. Can you compute it based on any other state or props in your component? If so, it isn’t state.

### How can you identify where state needs to live?

> Identify every component that renders something based on that state.
Find a common owner component (a single component above all the components that need the state in the hierarchy).
Either the common owner or another component higher up in the hierarchy should own the state.
If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component. 