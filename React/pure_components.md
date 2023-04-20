## Pure Component
1. Pure Components in React are the components which do not re-renders when the value of state and props has been updated with the same values
2. If the value of the previous state or props and the new state or props is the same, the component is not re-rendered.
- Features of React Pure Components
1. Prevents re-rendering of Component if props or state is the same
2. Takes care of “shouldComponentUpdate” implicitly
3. State and Props are Shallow Compared
4. Pure Components are more performant in certain cases

```
function Recipe({ drinkers }) {
  return (
    <ol>    
      <li>Boil {drinkers} cups of water.</li>
      <li>Add {drinkers} spoons of tea and {0.5 * drinkers} spoons of spice.</li>
      <li>Add {0.5 * drinkers} cups of milk to boil and sugar to taste.</li>
    </ol>
  );
}

export default function App() {
  return (
    <section>
      <h1>Spiced Chai Recipe</h1>
      <h2>For two</h2>
      <Recipe drinkers={2} />
      <h2>For a gathering</h2>
      <Recipe drinkers={4} />
    </section>
  );
}
```
### Output
```
Spiced Chai Recipe
For two
1. Boil 2 cups of water.
2. Add 2 spoons of tea and 1 spoons of spice.
3. Add 1 cups of milk to boil and sugar to taste.
For a gathering
1. Boil 4 cups of water.
2. Add 4 spoons of tea and 2 spoons of spice.
3. Add 2 cups of milk to boil and sugar to taste.
```
