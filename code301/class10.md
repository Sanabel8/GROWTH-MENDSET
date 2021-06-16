Understanding the JavaScript Call Stack 

1. What is a ‘call’?
The call stack is primarily used for function invocation (call).
is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

2. How many ‘calls’ can happen at once?
3. What does LIFO mean?
 Last In, First Out,
 it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
```function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();```

5. What causes a Stack Overflow?
 when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.





JavaScript error messages

1. What is a ‘refrence error’?This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
This is also a common thing when using const and let

2. What is a ‘syntax error’?
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

3. What is a ‘range error’?
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

4. What is a ‘tyep error’?
 this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
This is probably the most frequent error in JS

5. What is a breakpoint?
The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

6. What does the word ‘debugger’ do in your code?
I’ve added a debugger statement and when running the code above you can see the “history” before reaching that breakpoint.