## How does React work?
1. React components are defined as JavaScript functions or classes that return a piece of UI, known as a "render output". The render output can be a DOM element, another React component, or even a string of text.
2. When a component is rendered, React creates a virtual representation of the component and its render output, known as the "virtual DOM". The virtual DOM is a lightweight copy of the actual DOM, and it is used to efficiently update the UI without directly manipulating the real DOM.
3. When the application state changes or the user interacts with the UI, React updates the virtual DOM to reflect the new state or input. This process is known as "reconciliation".
4. Once the virtual DOM is updated, React performs a "diffing" algorithm to compute the minimum number of changes required to update the real DOM to match the virtual DOM. This process is known as "re-rendering".
5. Finally, React updates the real DOM with the changes computed during the diffing algorithm.
