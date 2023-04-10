| Real DOM  | Virtual DOM |
| ------------- | ------------- |
| The real DOM is a tree-like structure that represents the current state of a web page in memory. | On the other hand, the virtual DOM is a lightweight representation of the real DOM. |
| It is constructed by the browser when the page is loaded, and it can be manipulated and updated using JavaScript. | It is a JavaScript object that mimics the structure of the real DOM but does not have any direct connection to the browser's rendering engine.Instead, it is maintained and updated by a JavaScript library or framework. |
| real DOM is slow to update | virtual DOM is fast |
|When changes are made to the real DOM, the browser must recalculate the layout and repaint the entire page, which can be a time-consuming process. | In contrast, the virtual DOM allows the library or framework to efficiently compare the current state of the virtual DOM to the previous state and determine the minimum number of updates needed to synchronize the real DOM with the virtual DOM. |
