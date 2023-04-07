## Lifecycle medthods
There are three phases of a component's lifecycle: Mounting, Updating, and Unmounting. 
### Mounting Phase: 
1.  Mounting phase is the first phase of a component's lifecycle, during which the component is initialized and added to the DOM.
2.  In other words, it is the process of creating a component and rendering it on the webpage.
3.  During the Mounting phase, ReactJS executes four lifecycle methods in the following order:
- constructor(): This method is called first and is used to initialize the component's state and bind event handlers. It takes in the props as an argument and initializes the component's state with a default value.
- static getDerivedStateFromProps(): This method is called second and is used to update the component's state based on the props received from the parent component. It is a static method, which means it cannot access the component's instance or props. It takes in the props and state as arguments and returns an object that represents the new state.
- render(): This method is called third and is used to render the component's UI based on the current state and props. It returns a React element, which is a lightweight description of what should be rendered on the webpage.
- componentDidMount(): This method is called fourth and is used to perform any side effects, such as making API calls or setting up event listeners. It is called immediately after the component is mounted in the DOM.
4. Overall, the Mounting phase is the process of creating a component, initializing its state and props, and rendering it on the webpage. It is an important phase that sets the foundation for the next phase, the Updating phase, during which the component's state and props may change.

### Updating Phase:
1. Updating phase is the second phase of a component's lifecycle, during which the component is updated based on changes to its state or props.
2. In other words, it is the process of updating a component's UI based on new data.
3. During the Updating phase, ReactJS executes five lifecycle methods in the following order:
- static getDerivedStateFromProps(): This method is called first and is used to update the component's state based on changes to its props. It takes in the props and state as arguments and returns an object that represents the new state.
- shouldComponentUpdate(): This method is called second and is used to determine whether the component should be re-rendered or not. It takes in the next props and state as arguments and returns a Boolean value that indicates whether the component should update or not.
- render(): This method is called third and is used to render the component's UI based on the updated state and props.
- getSnapshotBeforeUpdate(): This method is called fourth and is used to capture information about the component's current state, such as scroll position, which can be used later in the componentDidUpdate() method. It takes in the prev props and state as arguments and returns a snapshot value that can be used later.
- componentDidUpdate(): This method is called fifth and is used to perform any side effects, such as updating the DOM or making API calls, after the component has been updated. It takes in the prev props, prev state, and snapshot value as arguments.

### Unmouting phase:
