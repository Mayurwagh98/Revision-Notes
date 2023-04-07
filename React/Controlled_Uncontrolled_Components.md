## What are controlled components
1. In React, a controlled component is a form element, such as an input, textarea, or select, whose value is controlled by React through state. 
2. In other words, the value of the form element is stored in the component's state, and any changes to the value are also handled by React.
3. o make a component controlled, you need to define a state variable to store the value of the form element, and an onChange event handler to update the state whenever the user interacts with the form element.
```
import React, { useState } from "react";

function Input() {
  const [value, setValue] = useState("");

  const handleChange = (event) => {
    setValue(event.target.value);
  };

  return (
    <div>
      <label htmlFor="input">Input:</label>
      <input type="text" id="input" value={value} onChange={handleChange} />
      <p>You typed: {value}</p>
    </div>
  );
}

export default Input;
```
## What are uncontrolled components
1. In React, an uncontrolled component is a form element, such as an input, textarea, or select, whose value is handled by the browser's DOM instead of by React through state.
2. In other words, the value of the form element is not stored in the component's state, and any changes to the value are not handled by React.
3. To access the value of an uncontrolled component, you can use a ref to reference the DOM node and read its value property.
```
import React, { useRef } from "react";

function Input() {
  const inputRef = useRef(null);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log("Input value:", inputRef.current.value);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label htmlFor="input">Input:</label>
      <input type="text" id="input" ref={inputRef} />
      <button type="submit">Submit</button>
    </form>
  );
}

export default Input;
```
