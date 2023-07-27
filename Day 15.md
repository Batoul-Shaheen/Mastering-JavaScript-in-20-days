# Day 15: 💻

 **ADVANCED SCOPE & ClOUSER**

 ## Lesson Summary:

 - **`Const ->`** use const in specific cases, value doesn`t change, can`t be reassigned, reassign in array is alowed.
 - only use the const with one of the primitive immutable values.
  
 - **`Hoisting`** -> let doesn't hoist? false.
   
 - **`Closure`** -> is when a function “remembers” its lexical scope even when the function is executed outside that lexical scope.
 - so `clouser` is preservation of the likage to a variable not the capturing of the value.
   
 - **`Modules`** -> encapsulate data and behavior (methods) together. The state (data) of a module is held by its methods via closure.
 - `encapsulation` -> is a fancy solution CS word (idea of hiding data & behavior).
 - so you can`t have a module, if u don`t have a clouser.
 - `export default` is a feature in JavaScript modules that allows you to export a single value (function, object, or any other value) as the default export from a module.

## Challenges:
##### [Questions](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day4-tasks/tasks.md)

#### ADVANCED SCOPE:
##### QUESTION 1:
##### My solution :

```javascript
for (var i = 0; i < 5; i++) {
  (function (index) {
    setTimeout(function () {
      console.log("value of [i] is: ", index);
    }, 100);
  })(i);
}
```

##### QUESTION 2:
##### My solution :

```javascript
let array = []; 
for (let i = 0; i < 5; i++) {
   array.push(i); 
   console.log("Current array is: ", array);
}
```

##### QUESTION 3:
##### My solution :

```javascript
let functions = [];

for (let i = 0; i < 5; i++) { 
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());
```

#### Clouser
##### Question 1:
##### My solution:

```javascript
const privateCounter = () => {
  let count = 0;

  const increment = () => {
    count++;
  };

  const getCount = () => {
    return count;
  };

  return {
    increment,
    getCount,
  };
};


const counter = privateCounter();

counter.increment();
counter.increment();
console.log(counter.getCount()); 
```

##### Question 2:
##### My solution:

```javascript
const generateFibonacci = (count) => {
  let current = 0;
  let next = 1;
  let index = 0;

  const fibonacci = () => {
    if (index < count) {
      const result = current;
      [current, next] = [next, current + next];
      index++;
      return result;
    } else {
      return undefined; 
    }
  };

  return fibonacci;
};
```
