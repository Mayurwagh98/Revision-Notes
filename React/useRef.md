## What are useRefs? What are some usecases?
1. The useRef Hook allows you to persist values between renders.
2. It can be used to store a mutable value that does not cause a re-render when updated.
3. It can be used to access a DOM element directly.

```
const [inputValue, setInputValue] = useState("");
  const count = useRef(0);

  useEffect(() => {
    count.current = count.current + 1;
  });

  return (
    <>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <h1>Render Count: {count.current}</h1>
    </>
  );
}
```
useRef() only returns one item. It returns an Object called current.

When we initialize useRef we set the initial value: useRef(0).

It's like doing this: `const count = {current: 0}`. We can access the count by using count.current.
