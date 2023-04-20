## What are useEffect and useRef?

### useEffect: 

1. useEffect is a hook in React that allows functional components to perform side effects, such as fetching data, subscribing to events, or updating the DOM, after the component has rendered.
2. It is similar to lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount in class components.

### useRef: 

1. useRef is a hook in React that allows functional components to create and maintain a reference to a mutable value that persists across renders. 
2. It is commonly used to get a reference to a DOM element, store a mutable value that doesn't trigger re-renders, or cache a value that needs to be persisted across renders.
3. useRef returns a mutable ref object with a current property that can be used to store and access the mutable value.
4. The `current` property can be updated without triggering a re-render of the component.
```
import React, { useRef, useState, useEffect } from "react";

export default function App() {
  const inputRef = useRef(null);
  let [inputvalue, setInpuTvalue] = useState("");

  const handleButtonClick = () => {
    // Access input value using ref
    setInpuTvalue(inputRef.current.value);
    // console.log("Input value:", );
  };
  return (
    <>
      <input ref={inputRef} type="text" />
      <button onClick={handleButtonClick}>Get Input Value</button>
      <h1>{inputvalue}</h1>
    </>
  );
}

```
