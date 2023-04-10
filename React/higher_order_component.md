- Higher Order Component (HOC) is a function that takes a component and returns a new component with additional functionality or props.
- HOCs allow for code reuse and composability in React applications.
- Imagine you have a component that needs to make an API call to retrieve data. Instead of duplicating the code to make the API call in every component that needs it, you can create a HOC that handles the API call and passes the data as props to the wrapped component.
- Here's an example of a simple HOC that adds a "loading" prop to a component:
```
function withLoading(Component) {
  return function(props) {
    const [isLoading, setLoading] = useState(true);

    useEffect(() => {
      setLoading(false);
    }, []);

    return <Component {...props} loading={isLoading} />;
  }
}
```
- You can use this HOC like this:
```
function MyComponent(props) {
  // ...
}

const MyComponentWithLoading = withLoading(MyComponent);
```
- Now, when you render MyComponentWithLoading, it will receive a loading prop that indicates whether the component is currently loading or not.
- HOCs can be used for many different purposes, such as adding authentication, logging, or other functionality to components.
