## Pure Component
1. Pure Components in React are the components which do not re-renders when the value of state and props has been updated with the same values
2. If the value of the previous state or props and the new state or props is the same, the component is not re-rendered.
- Features of React Pure Components
1. Prevents re-rendering of Component if props or state is the same
2. Takes care of “shouldComponentUpdate” implicitly
3. State and Props are Shallow Compared
4. Pure Components are more performant in certain cases
