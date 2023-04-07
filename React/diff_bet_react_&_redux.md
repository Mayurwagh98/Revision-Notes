## Difference between React and Redux.
1. Purpose: React is focused on building user interfaces, while Redux is focused on managing the application state.
2. Architecture: React uses a component-based architecture, where UI components are defined as self-contained pieces of code. Redux uses a centralized architecture, where the application state is managed in a single store.
3. State Management: React manages the UI state of the application within the component itself. Redux manages the application state in the store, and components receive the state they need as props.
4. Data Flow: React follows a one-way data flow, where props are passed down from parent to child components. Redux also follows a one-way data flow, where actions are dispatched to the store, which updates the state and notifies subscribers of the change.
