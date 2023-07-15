# Day 12 : 💻

Types & Coercion.

## Lesson Summary :

- In JavaScript, everything is an object  -> false
- In JavaScript, variables don't have types, values do.
- var v = null ; typeof null -> object.
- var a = [1,2,3] ; typeof a -> object.
- var y = 42n ; typeof y -> Bigint.
- if the variable doesn`t have a value, the typeof is undefined.

`undefined vs. undeclared vs. uninitialized`
- undefine: didn`t exist.
- undeclared: its never been created in any scope.
- uninitialized: variable in block scope  don`t ge initialized.

- `NaN` -> not a number,
Invalid Number
 {undefined , null ,  false , -1 , 0}
- NaN are not equle itself.
- undefined are equal itself

- `Negative Zero`
```javascript
var v = -0;
v.toString(); //0
```
- use new -> Object() , Array() , Function() , Date() ,RegExp() , Error().
- Don't use new -> String() , Number() , Boolean().

- `ToString ()`
- null  -> "null"
- undefined -> "undefined"
- true -> "true"
- false -> "false"
- 3.14159 -> "3.14159"
- 0 -> "0"
- -0 ->  "0"
- [] -> ""
- [1,2,3] -> "1,2,3"
- [null,undefined] ->  ","
- {} -> "[object Object]"
- {a:2} -> "[object Object]"

- `ToNumber()`
- "" -> 0
- "0" -> 0
- "-0" -> -0
- " 009 " -> 9
- "3.14159" -> 3.14159
- "0." -> 0
- ".0" -> 0
- "." -> NaN
- false -> 0
- true -> 1
- null -> 0
- undefined -> NaN
- [null] -> 0
- [undefined] -> 0
- [1,2,3] -> NaN

- `toBoolean` ->  if it`s not that the list in Falsy it is always truthy
- Falsy : "" , 0, -0 ,null , NaN , false , undefined

## Challenges :







