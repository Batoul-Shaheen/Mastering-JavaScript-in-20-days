# Day 9: 💻

**closure**

## Lesson Summary:

`closure` is the function that preserves the outer scope in it`s inner scope.

What can we call this `‘backpack’`?
- Closed over ‘Variable Environment’ (C.O.V.E.)
- Persistent Lexical Scope Referenced Data (P.L.S.R.D.)
- ‘Backpack’
- ‘Closure’

## Challenges:
#### [Questions for closure](https://github.com/orjwan-alrajaby/gsg-expressjs-backend-training-2023/blob/f1770252e28aab81cc91fe65db1ef2cf1dca6b37/learning-sprint-1/week2-day2-tasks/tasks.md)

#### [Question 1] 
##### my solution:

```javascript
function createCounter(start) {
   let counter = start;
      function incrementCounter(){
        counter++;
        return counter;
    }
    return incrementCounter
}

const increment = createCounter(5);
```

#### [Question 2]
##### my solution:

```javascript
function calculateAverage (array){
        let sum = 0;
        for( let i = 0 ; i < array.length ; i++ ){
            sum += array[i];
         }
        function average() {
            return sum / array.length;
        }

        return average;
}


const Avg = calculateAverage([1,2,3,4,5,6] );
```

#### [Question 3]
##### my solution:

```javascript
function powerOf(base) {
    return function(exp) {
      return Math.pow(base, exp);
    };
  }
  
  const powerOfTwo = powerOf(3);
  console.log(powerOfTwo(4)); 
  ```

#### [Question 4]
##### my solution 

```javascript
function compose(...functions) {
    return function(input) {
      let result = input;
  
      for (let i = functions.length - 1; i >= 0; i--) {
        result = functions[i](result);
      }
  
      return result;
    }
  }
```
