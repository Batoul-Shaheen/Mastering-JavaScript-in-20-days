# Day 13: 💻

**Static typing & scope**

## Lesson Summary:

**`typeScript:`** Extremely popular these days, will make your code more readable and more robust.
- in ts, if u have types, u can either ignore types entirely and use triple equals.


```typescript
var teacher: string = "Batool";
teacher = {name:"Eleen"};  // Eroor can`t assign object to string
```

**`Scope:`** 
- JS is not an interpreted language it is a compiled language (line by line).
- in Js have function & blocks, those are the units of scope.
- in the compilation phase we have ->  scope manager &  virtual machine.
- What kind of ref to a marble? source, target.
- `source` -> receiving a value.
- `target` -> retrieve its value.
- all of the lexical scopes & identifiers that are all determined at compile time.
- source vs target position at compile time but we don`t use that info until run time.
- in the console, if u have a variable as an argument it is -> source position.
- `undeclare` -> never formally declared in any scope that we have accessed to(don`t have a marble for it) & in strict mode it always results in that ref area
- `undeclare & undefined` -> are doesn`t exist but undefined doesn`t have a value.

## Challenges:
##### [Questions](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/main/learning-sprint-1/week3-day2-tasks/tasks.md)

##### STATIC TYPING QUESTIONS:

##### Question 1:

```typescript
interface HelloWorldPromise {
  (): Promise<string>;
}

interface BooleanCheckPromise {
  (boolean: boolean): Promise<boolean>;
}

interface ReturnObjPromise {
  (): Promise<{ x: string; y: number }>;
}

type PromisesArray = [HelloWorldPromise, BooleanCheckPromise, ReturnObjPromise];

const sayHelloWorld: HelloWorldPromise = () =>
  new Promise((resolve, reject) => {
    resolve("Hello world!");
  });

const checkBoolean: BooleanCheckPromise = (boolean) =>
  new Promise((resolve, reject) => {
    if (boolean) {
      resolve(boolean);
    } else {
      reject(`Input is false :(`);
    }
  });

const returnObj: ReturnObjPromise = () =>
  new Promise((resolve, reject) => {
    resolve({
      x: "meow",
      y: 45,
    });
  });

const promisesArray: PromisesArray = [sayHelloWorld, checkBoolean, returnObj];

const convertToObj = async (array: PromisesArray) => {
  const obj = {};
  for (const promise of array) {
    const result = await promise();
    Object.assign(obj, result);
  }
  return obj;
};
```

##### SCOPE & HOISTING QUESTIONS:

##### Question 1:

```javascript
// What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.

function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();
```

##### My solution is :

- 1, ReferenceError, ReferenceError.
- **`explain`** var has function scope, so it is accessible within the entire testScope1 function, let & const has block scope, It is only accessible within the if block.

##### Question 2:

```javascript
// What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.

function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();
```

##### My solution is :
- undefined, ReferenceError, ReferenceError.
- **`explain`** variable a (var) is hoisted to the top of the function scope, let and const have block scope, It is not hoisted to the top of the block.

##### Question 3:

```javascript
// What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.

function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();
```

##### My solution is :
- [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1,100, 45 ]
- **`explain`** The first console.log refers to the outer variables, The second console.log inside the if block refers to the newly declared variables,The third console.log after the if block, the outer variables have been modified by the inner block







