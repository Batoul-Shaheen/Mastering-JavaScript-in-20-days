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
### [Compound Assignment With Augmented Multiplication:](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)
#### My Solution
```
let a = 5;
let b = 12;
let c = 4.6;

a *= 5;
b *= 3;
c *= 10;
```

### [Concatenating Strings with the Plus Equals Operator:](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)
#### My Solution
```
let myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";
```

### [Use Bracket Notation to Find the Nth-to-Last Character in a String:](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)
#### My Solution
```
const lastName = "Lovelace";
const secondToLastLetterOfLastName = lastName[lastName.length - 2]; 
```



  
    
