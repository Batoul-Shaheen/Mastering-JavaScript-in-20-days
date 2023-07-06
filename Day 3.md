# Day 3: 💻

Expression & Arrays 

## Lesson Summary:

in JavaScript, you can declare variables with the var, let, and const keywords.

**Expression vs. statement:**
- An expression asks JS for a value
- A statement tells to do sth (e.g declare/assign a variable)

**Arrays:**
 - arrays let us keep multiple values together in a single collection.
 - arrays can be empty.
 - arrays can hold any type of item, or mix & match.
   
**Some methods used in Arrays:**
 - length: find out the length of an array.
 - includes: returns true if an array contains a specified value.
 - push: to add one or more items to the end of an array.
 - pop: to remove the last item from the array.
 - sort: allows you to sort elements of an array in place.
 - join: creates and returns a new string by concatenating all of the elements in an array, separated by commas or a specified separator string.
 - concat: is used to merge two or more arrays, this method does not change the existing arrays but instead returns a new array.

**mutable vs. immutable**
 - "Mutable" data can be edited (e.g. Arrays), "Immutable" data is always the same (e.g. string & other primitives)
 - if u have the choice, using immutable data & variables is usually best.

### Challenges:
### [Profile Lookup:](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)
#### My Solution
```

const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line
  for(let i=0 ; i < contacts.length ; i++){
  if (contacts[i].firstName === name){
    if (prop in contacts[i]){
    return contacts[i][prop];
    }else {
     return "No such property";
    }
   }
  }
  return"No such contact";
  // Only change code above this line
}
lookUpProfile("Akira", "likes");
```

### [Copy Array Items Using slice():](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)
#### My Solution
```

function forecast(arr) {
  // Only change code below this line
  return arr.slice(2, 4);
}
// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

### [Combine Arrays with the Spread Operator:](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)
#### My Solution
```

function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment, 'is', 'fun' ]; // Change this line
  return sentence;
}
console.log(spreadOut());
```


  
