# Day 11:

Classes & Prototypes

## Lesson Summary:

 **What techniques do we have for creating objects?**
 - Declare an empty object and add properties with dot notation.

```javascript
const user = {}; // creat an empty object
```

-Creating user using Object.create.

```javascript
const user = Object.create(null);
```

**Our code is getting repetitive, we're breaking our DRY principle. And suppose we have millions of users! What could we do?**
- Solution 1: Generate objects using a function.

```javascript
function userCreator(name, score) {
 const newUser = {};
 newUser.name = name;
 newUser.score = score;
 newUser.increment = function() {
 newUser.score++;
 };
 return newUser;
};
const user = userCreator("Will", 3);
user.increment()
```

- Solution 2: Using the prototype chain, Make the link with Object.create() technique

```javascript
function userCreator (name, score) {
 const newUser = Object.create(userFunctionStore);
 newUser.name = name;
 newUser.score = score;
 return newUser;
};
const userFunctionStore = {
 increment: function(){this.score++;},
 login: function(){console.log("Logged in");}
};
const user = userCreator("Will", 3);
user.increment();
```

- Solution 3: Using the keyword new.
1. Create a new user object.
2. Return the new user object.

```javascript
const user = new userCreator("Batool", 3);
```

- Solution 4: Using the class.

```javascript
class UserCreator {
 constructor (name, score){
 this.name = name;
 this.score = score;
 }

 increment (){ this.score++; }
 login (){ console.log("login"); }
}
const user = new UserCreator("Ellen", 9);
user.increment();
```

## Challenges:
#### [Object Oriented Programming](https://www.freecodecamp.org/batool-shaheen)
