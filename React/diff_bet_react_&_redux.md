## Difference between React and Redux.
| | React | Readux |
| ----- | ----- | ------|
| Purpose | React is focused on building user interfaces | Redux is focused on managing the application state |
| Architecture | React uses a component-based architecture, where UI components are defined as self-contained pieces of code | Redux uses a centralized architecture, where the application state is managed in a single store |
| State Management | React manages the UI state of the application within the component itself | Redux manages the application state in the store, and components receive the state they need as props |
| Data Flow | React follows a one-way data flow, where props are passed down from parent to child components | Redux also follows a one-way data flow, where actions are dispatched to the store, which updates the state and notifies subscribers of the change |

