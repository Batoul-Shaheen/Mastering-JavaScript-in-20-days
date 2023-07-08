# Day 6: 💻

Data Fetching & Promises, Destructuring Data, Async.

## Lesson Summary:

### Data Fetching & Promises:

- `fetching data:` get data from the internet using URLs.
- fetch("URLs") use to load data from APIs, but if we run it in the console, we see sth weird.
- `APIs:` application programming interfaces.
- APIs provide URLs that point to data we care about.
- `promises:` use with APIs.
- Promises can be in 3 possible states:
1. pending: still waiting for the value, hang tight.
2. fulfilled (aka "resolved"): finally got the value, all done.
3. rejected: sorry couldn't get the value, all done It takes time for Promises to resolve, so they are "asynchronous".
- we put the word await before our call to fetch -> wait for the promise to be done, and then give me the value of the promise, fetch return a response object

#### syntax:

```javascript
let response = await fetch("https://....");
console.log(response);
```

- the browser send a request.
- `responses have a method called JSON:` parses its body as a JSON object

#### syntax:

```javascript
response.json();
```

Let's try, this time awaiting the JSON Promise too.

#### syntax:

```javascripe
let response = await fetch("https://...");
let body = await response.json();
```

### Destructuring Data:

- Destructuring is a fancy way of declaring multiple variables at once.
- By "extracting" values from an object with their property names.

#### syntax:

```javascript
let {name, nickname} = spices[0];
```

- If we only care about some of the properties, we can omit the others.

#### syntax:

```javascript
let {nickname} = spices[2];
```

-We can also destructure Arrays, assigning variables for their items.

#### syntax:

```javascript
const [baby, ginger, scary, sporty, posh] = spices;
```

- We can ignore the values in the array we don't need use commas.

#### syntax:

```javascript
const [,,melB] = spices;
```

- We can use ... to collect remaining values.

#### syntax:

```javascript
const [babySpice, ...adultSpices] = spices;
```
