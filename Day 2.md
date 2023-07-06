# Day2: 💻
 On this day I will talk about values, Data Types & Operator


## Lesson Summary:
 - typeof => tells you the type of a value.
  
 **JS has two kinds of Data:**
  1. Primitive types(e.g string,number,boolean,undefined,null).
  2. Objects.
  - typeof null => Object
  - typeof "" => string

 **some function used at sting:**
 
 - indexOf: used for what is the index of a specific character & At what index does this substring begin.
 - includes: used for Does the string include some other string.
 - startsWith: used for Does the string start with some other string.

  **Operator:** 
  
  we used (+) to concat the string
  
  **strict vs lossey-gossey:**

| Strict | lossey-gossey | Meaning |
| ----------- | ----------- |  -----------|
| === | == | equals |
| !== | != | doesn`t equal |

you should almost always use the strict version

- Logical OR(||)
- Logical AND(&&)
- Increment(++)
- decrement(--)

  
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




  
    
