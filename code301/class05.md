Putting it all together
Thinking in React
1. How would you break a mock into a component heirarchy?
. draw boxes around every component and give them all names ==name of react component.

2. What is the single responsibility principle and how does it apply to components?
a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.
the same techniques for deciding if you should create a new function or object

3. What does it mean to build a ‘static’ version of your application?
it’s away to implement your app and renders your data model,
4. Once you have a static application, what do you need to add?

5. What are the three questions you can ask to determine if something is state?
* Is it passed in from a parent via props? If so, it probably isn’t state.
* Does it remain unchanged over time? If so, it probably isn’t state.
* Can you compute it based on any other state or props in your component? If so, it isn’t state.

6. How can you identify where state needs to live?
. Identify every component that renders something based on that state.
. Find a common owner component (a single component above all the components that need the state in the hierarchy).
. Either the common owner or another component higher up in the hierarchy should own the state.
. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.



*React learn us how using think about apps as you build them.

process of building a searchable product data table using React:
1. Break The UI Into A Component Hierarchy
2. Build A Static Version in React
3. Identify The Minimal (but complete) Representation Of UI State
4. Identify Where Your State Should Live
5. Add Inverse Data Flow






















