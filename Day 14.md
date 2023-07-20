# Day 14:  💻

**Scope & Function Expressions**

## Lesson Summary:

**- different btw anonymous function expression & named function expression**
1. `Anonymous functions` don't have a name. But, `named functions` can reference themselves using their own name.
2. `Named function expressions` are often more useful for debugging purposes, whereas `anonymous functions` may appear as (anonymous) in stack traces.
- if every function has a purpose it means every function has a name.
- arrow function is anonymouse.
- differencse in code readability and functionality btw using named functions & using arrow function.
- `IIFE` ->  Immediately Invoked Function Expression, that allows you to create and execute a function immediately after its declaration, often used to create a 
 private scope for variables and functions, preventing them from polluting the global scope.

##### Syntax:

```javascript
(function () {

})();
```
- Using block scoping instead of IIFE.
- lexical scope -> related to compiler.


## Challenges:
##### [Questions](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day3-tasks/tasks.md)

##### Question 1:
##### My solution:

```javascript
const arrowHOF = (normalFunc) => {
  return (...args) => {
    return (...multiplierArgs) => {
      return normalFunc(...args) * multiplierArgs.length;
    };
  };
};
```

##### Question 2:
##### My solution:

```javascript
const preserveThis = (func) => {
  return (...args) => {
    return func.apply(func, args);
  };
};
```

##### Question 3:
##### Example 1:

```javascript
Example 1:

function outer1() {
  var x = 10;

  var inner1 = function() {
    console.log(x);
  };

  inner1();
}

outer1(); // Output: 10
```
##### My solution:
- Reason: var declaration in the global scope.

##### Example 2 :

```javascript
function outer2() {
  var x = 10;

  var inner2 = function() {
    var x = 20;
    console.log(x);
  };

  inner2();
}

outer2(); // Output: 20
```
##### My solution:
- Reason: var declaration in global & local scope, but when console there is var declaration in local scope.
