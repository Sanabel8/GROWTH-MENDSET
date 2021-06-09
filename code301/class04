React Docs - Forms

1. What is a ‘Controlled Component’?
.controlled component: An input form element whose value is controlled by React by making the React state be the “single source of truth” and only updated with setState().

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
 Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

3. How do we target what the user is entering if we have an event handler on an input field?
When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name



* the displayed value will always be this.state.value ,making the React state the source of truth.
* In React, a <textarea> uses a value attribute instead. This way, a form using a <textarea> can be written very similarly to a form that uses a single-line input:
* ```<input type="text">
<textarea>
<select>```
 all work very similarly - they all accept a value attribute that you can use to implement a controlled component.
* You can pass an array into the value attribute, allowing you to select multiple options in a select tag:
```<select multiple={true} value={['B', 'C']}>```
* The file input Tag :t is an uncontrolled component in React,Because its value is read-only

The Conditional (Ternary) Operator Explained
1. Why would we use a ternary operator?
for decision making in place of longer if and else conditional statements.
2. Rewrite the following statement using a ternary statement
```if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }```
``` function = (x===y) ? true :false ; ```

* the ternary operator: condition ? value if true : value if false