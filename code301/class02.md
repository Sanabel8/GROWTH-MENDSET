React: Component Lifecycle Events

components :is classes or functions .
lifecycle events : The methods that you are able to use on components or classes
* we can call the method during the lifecycle of component, and use it to update the ul and application states.
* phases of the component lifecycle:
1. mounting.
* Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.

2. updating.

static getDerivedStateFromProps, 
shouldComponentUpdate, 
render,
getSnapshotBeforeUpdate,
componentDidUpdate, 
UNSAFE_componentWillUpdate, 
UNSAFE_componentWillReceiveProps

3. unmounting.
* when a component is being removed from the DOM , it is occure.
* componentWillUnmount its the only life cycle

* constructor() :IT is called before it is mounted 
* super(props : to call the subclass 
* to assign state we used constructors using this.state
* Avoid using this.setState() in the constructor

* static getDerivedStateFromProps(): This method exists for rare cases where the state relies on changes in props over time.
* render() only required method in a class component.
*  The render function should not modify the component state
* componentDidMount() : This method is invoked immediately after a component is mounted and it used to set up any subscriptions


