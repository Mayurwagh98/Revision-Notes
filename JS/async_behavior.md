## asyncrnonous behavior in javascript
  
  https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing
  
Asynchronous programming is a technique that enables your program to start a potentially long-running task and still be able to be responsive to other events while that task runs, rather than having to wait until that task has finished. Once that task has finished, your program is presented with the result.

  - setTimeout
  The global setTimeout() method sets a timer which executes a function or specified piece of code once the timer expires.
  ```
  setTimeout(() => {
  console.log("Delayed for 1 second.");
}, 1000)
  ```
  - setInterval
The setInterval() method, offered on the Window and Worker interfaces, repeatedly calls a function or executes a code snippet, with a fixed time delay between each call.
```
  <h1 class="heading">Hello</h1>
  <button class="start">start</button>
  <button class="stop">stop</button>
  
  let heading = document.querySelector(".heading"); 
  let id;
  let start = document.querySelector(".start");
  start.addEventListener("click", () => {
    id = setInterval(() => {
      heading.textContent = Math.ceil(Math.random() * 10)
      
    }, 1000);
  });

  let stop = document.querySelector(".stop");
  stop.addEventListener("click", () => {
    clearInterval(id);
  });
```
