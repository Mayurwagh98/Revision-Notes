## What is Context API
1. The Context API helps share data between components which you can’t easily share with props, for example, complex data objects.  
2. React Context API provides a way to send data like userid, auth, and theme data through the component tree without sending any props manually at every level. 
3. We can also share specific states with multiple components instead through props manually. In some use cases, ideal for theming, localization, authentication etc.
```
import React, { createContext, useState } from "react";

// create a context
export const ThemeContext = createContext();

// create a provider
export const ThemeProvider = ({ children }) => {
  const [theme, setTheme] = useState("light");

  const toggleTheme = () => {
    setTheme(theme === "light" ? "dark" : "light");
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};

// example usage
const App = () => {
  return (
    <ThemeProvider>
      <Navbar />
      <Content />
    </ThemeProvider>
  );
};

const Navbar = () => {
  return (
    <ThemeContext.Consumer>
      {({ theme, toggleTheme }) => (
        <nav className={theme}>
          <button onClick={toggleTheme}>Toggle Theme</button>
        </nav>
      )}
    </ThemeContext.Consumer>
  );
};

const Content = () => {
  return (
    <ThemeContext.Consumer>
      {({ theme }) => <div className={theme}>Content goes here</div>}
    </ThemeContext.Consumer>
  );
};
```
### Counter
```
import React, { createContext, useContext, useState } from 'react';

// Step 1: Create a context
const CounterContext = createContext();

// Step 2: Create a provider component
function CounterProvider({ children }) {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(prevCount => prevCount + 1);
  };

  const decrement = () => {
    setCount(prevCount => prevCount - 1);
  };

  const value = {
    count,
    increment,
    decrement
  };

  return (
    <CounterContext.Provider value={value}>
      {children}
    </CounterContext.Provider>
  );
}

// Step 3: Create custom hooks to access the context
function useCounter() {
  return useContext(CounterContext);
}

// Step 4: Use the counter in components
function CounterDisplay() {
  const { count } = useCounter();

  return <div>Count: {count}</div>;
}

function CounterButtons() {
  const { increment, decrement } = useCounter();

  return (
    <div>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
}

// Step 5: Use the provider component at the top level of your app
function App() {
  return (
    <CounterProvider>
      <CounterDisplay />
      <CounterButtons />
    </CounterProvider>
  );
}

export default App;
```
