# Day 1: 💻

DOM (Document Object Model) 
  
## Lesson Summary:

- document.body: the body element.
- document.title: the page title.
- document.body.children: all the elements within the body.
- document.getElementById("board") || document.querySelector("#board"): the first element with id "board".
- document.getElementsByTagName("h1") ||  document.querySelectorAll("h1"): all the h1 elements.
- document.getElementsByClassName("player") || document.querySelectorAll(".player"): all the elements with class = "player".
- document.getElementsByClassName("player").length || document.querySelectorAll(".player").length: number of elements with class = "player".
- document.getElementById("p1-name").textContent: the text inside the element with id = "p1-name".
  
**- Editing the DOM with JS:**
- document.title="New Title": change the page title
- document.getElementById("#p1-name").textContent="batool": replace the text of the #p1-name element.
- document.getElementById("p1-name").append(" & friend"): add to the end of the elements current text.

### Coding Exercises:
```html
//Exercise1: Finding Element
//1.all the p elements
//2. the text "X"
//3. the number of squares in the board
//4. the text "A game you know"

document.getElementsByName("p")
document.getElementById("p1-symbol").textContent
document.querySelectorAll(".square").length
document.querySelector("h2").textContent

//Exercise2: Changing a web page 
//1. Change the player names to you & neighbor
//2. Swap the player symbols
//3. Change subtitle to "A game you know and love"

document.querySelector("#p1-name").textContent = "Baraa"
document.querySelector("#p2-name").textContent = "Lamees"
document.getElementById("#p1-symbol").textContent = "A"
document.getElementById("#p2-symbol").textContent = "L"
document.querySelector("header h2").textContent = "A game you know and love"

```






