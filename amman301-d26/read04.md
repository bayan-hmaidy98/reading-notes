# Forms 

### What is a ‘Controlled Component’?

React found another way to deal with submitted forms in html (form has the default HTML form behavior of browsing to a new page when the user submits the form.) You can -using the react- submit the form and acssess the data entered by the user in JS function. It is called `controlled components`

### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why?

No, it is updated when entered. `the displayed value will always be this.state.value, making the React state the source of truth. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.`

### How do we target what the user is entering if we have an event handler on an input field?

When creating `this.state` we can make a variable inside it (empty) and update it using event.value when entered. 


# JavaScript — The Conditional (Ternary) Operator Explained

### Why would we use a ternary operator?

`Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.`
 
### Rewrite the following statement using a ternary statement:

` if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }`

`(x===y) ?  console.log(true) : console.log(false) `
