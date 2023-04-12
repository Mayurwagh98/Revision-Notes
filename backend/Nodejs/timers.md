1. In Node.js, timers are functions that allow you to schedule the execution of a piece of code to occur after a certain amount of time has elapsed, or to repeatedly execute a piece of code at a set interval.
2. There are three types of timers in Node.js:
 - `setTimeout`: This timer is used to execute a function once, after a specified number of milliseconds has elapsed.
 - `setInterval`: This timer is used to repeatedly execute a function at a set interval, specified in milliseconds.
 - `setImmediate`: This timer is used to execute a function immediately after the current phase of the event loop completes.
3. Here's an example of how you can use timers in Node.js:

```
// Set a timer to execute a function after 2 seconds
const timeout = setTimeout(() => {
  console.log('Timer expired!');
}, 2000);

// Set an interval to repeatedly execute a function every 1 second
const interval = setInterval(() => {
  console.log('Interval expired!');
}, 1000);

// Set an immediate timer to execute a function immediately after the current phase of the event loop completes
setImmediate(() => {
  console.log('Immediate timer expired!');
});

// Clear the timeout after 3 seconds
setTimeout(() => {
  clearTimeout(timeout);
  console.log('Timeout cleared!');
}, 3000);

// Clear the interval after 5 seconds
setTimeout(() => {
  clearInterval(interval);
  console.log('Interval cleared!');
}, 5000);
```
### Output
```
Immediate timer expired!
Interval expired!
Timer expired!
Interval expired!
Timeout cleared!
```
