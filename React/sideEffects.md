## What are sideeffects
1. When we talk about side effects in the context of React.js, we are referring to anything that is outside the scope of React
2. So calling any native Web APIs will be considered as a side effect as it’s not within the React universe
3. Making a HTTPS request to an external API is another example of a side effect and the list goes on…
4. We usually manage React side effects inside the useEffect hook (part of the React Hooks API)
