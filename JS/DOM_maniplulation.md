## DOM Manipulation
1. createElement
```
const para = document.createElement("p");
para.innerText = "This is a paragraph";
document.body.appendChild(para);
```
2. getElementById
```
const myElement = document.getElementById("demo");
myElement.style.color = "red";
```
3. querySelector
```
document.querySelector("p");
```
4. querySelectorAll
```
var inputBoxes = document.querySelectorAll("input");
```
5. setAttribute
```
element.setAttribute("class", "democlass");
```
## event API
- The Event interface represents an event which takes place in the DOM.
- An event can be triggered by the user action e.g. clicking the mouse button or tapping keyboard, or generated by APIs to represent the progress of an asynchronous task.

## eventListener
- The addEventListener() method of the EventTarget interface sets up a function that will be called whenever the specified event is delivered to the target.
- addEventListener(type, listener)