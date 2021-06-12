Lists and Keys

1. What does .map() return?
alist 
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
* You can build collections of elements and include them in JSX using curly braces {}.
* by using the JavaScript map() function.
```const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);```

the reuslt will apeare as alist of elements .

3. Each list item needs a unique _keys_Among Siblings__.

4. What is the purpose of a key?
A “key” is a special string attribute you need to include when creating lists of elements.
Keys help React identify which items have changed, are added, or are removed.

```const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);```

* The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys:
* When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort:
* we don’t recommend using indexes for keys if the order of items may change.
* Keys only make sense in the context of the surrounding array.
* Keys Must Only Be Unique Among Siblings


The Spread Operator
1. The Spread Operator?
- useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.
- in JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.

2. List 4 things that the spread operator can do.

. Copying an array
. Concatenating or combining arrays
. Using Math functions
. Using an array as arguments
. Adding an item to a list
. Adding to state in React
. Combining objects
. Converting NodeList to an array

3. Give an example of using the spread operator to combine two arrays.
```let arr1 = [0, 1, 2];
let arr2 = [3, 5, 7];
let primes = [...arr1, ...arr2];

// > [0, 1, 2, 3, 5, 7]```

4. Give an example of using the spread operator to add a new item to an array.
```const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]```

5. Give an example of using the spread operator to combine two objects into one. 
```const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂```



