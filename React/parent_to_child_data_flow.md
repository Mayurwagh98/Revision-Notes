// Parent component
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  const greeting = "Hello, world!";
  
  return (
    <ChildComponent greeting={greeting} />
  );
}

export default ParentComponent;


// Child component
import React from 'react';

function ChildComponent(props) {
  return (
    <div>{props.greeting}</div>
  );
}

export default ChildComponent;
