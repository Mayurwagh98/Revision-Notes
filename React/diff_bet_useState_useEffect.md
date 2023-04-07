## What is the difference between useState and useEffect?
1. useState is a hook in React that allows functional components to manage local state.
2. It returns an array with two values: the current state value and a function to update the state.
```
import React, { useState } from 'react';

function CounterComponent() {
  const [count, setCount] = useState(0); // Initial state value is 0

  const increment = () => {
    setCount(count + 1); // Update count state
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```
useEffect: 
1. useEffect is a hook in React that allows functional components to perform side effects, such as fetching data, subscribing to events, or updating the DOM, after the component has rendered.
