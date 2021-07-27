# States and Props

## React Lifestyle

1. `render()` takes a place before `componentDidMount()`
2. Building the constuctor and have instances from it.
3. `constructor`
`render`
`componentDidMount`
`React Updates`
`componentWillUnmount`

4. >This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount().

### React State Vs Props

1. pass variables from one to another component down the component tree. (**integers over objects to arrays**)

2. Props: handled outside the component
state: inside the component

3. Changing something in the application (state)

4. User data


