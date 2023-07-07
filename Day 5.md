# Day 5: 💻

Events & Handlers & Conditions.

## Lesson Summary:

### **Events & Handler**

We can detect events with JS using an event listener The `.addEventListener()` method
- `.addEventListener()` takes 2 parameters:
1. The name of the event to listen to (e.g. "click")
2. A handler function that JS calls when that event is fired on this element

```javascript 
document.addEventListener("click", () => {
    console.log("clicked")
});
```

- type of event:
1. "click".
2. "dblclick".
3. "mouseover".
4. "mouseout".

### **Conditions**

`if else statements` > if statement: if they`re not-empty if they have some characters inside of them, they`re truthy.

`empty arrays: ` are trythy but `empty strings` > are falsy.

`null & undefined: `  are falsy.

`Conditional ternary operator> ` condition ? valueIfTrue : valueIfFalse;

`for ... of`

```javascript
for (let char of "ALOHA") {
    console.log(char); 
}
```

### **map, filter & spread**

The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array.

##### syntax:

```javascript
map(callbackFn)
map(callbackFn, thisArg)
```

`String templates` are useful, make them with backticks and ${} 

##### syntax:

```javascript
`string to insert ${variable} into`
```

`filter` calls a true/false function on each item, and creates a new array with only the items where the function returns true.

##### syntax:

```javascript
filter(callbackFn)
filter(callbackFn, thisArg)
```
`Spread (...)` We can use it to put all the items from one array inside another array & also use it to pass all the items from an array as arguments to a function or method

`JS can only do one task at a time`

- Some things that take time:

1. Waiting for user events
2. Asking a user to pick a file
3. Getting permission to access the camera/mic
4. Loading data from the interwebs


## Challenges:




