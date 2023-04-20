```
// Parent component
import React, { useState } from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  const [message, setMessage] = useState("");

  const handleMessage = (messageFromChild) => {
    setMessage(messageFromChild);
  };

  return (
    <div>
      <p>Message from child: {message}</p>
      <ChildComponent handleMessage={handleMessage} />
    </div>
  );
}

export default ParentComponent;


// Child component
import React from 'react';

function ChildComponent(props) {
  const handleClick = () => {
    props.handleMessage("Hello from child!");
  };

  return (
    <button onClick={handleClick}>Send message to parent</button>
  );
}

export default ChildComponent;
```
