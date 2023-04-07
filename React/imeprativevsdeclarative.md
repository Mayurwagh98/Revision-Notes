https://egghead.io/blog/wtf-is-declarative-programming

- Imperative
Imperative programming your code shows exactly how to do what you want to happen.
```
const root = document.getElementById('root')
const container = document.createElement('section')
const title = document.createElement('h1')
container.id = 'new'
title.innerText = 'Welcome to Our Page!'
container.appenedChild(title)
root.appendChild(container)
```

- Declarative 
In simple terms, declarative programming is when your code shows what you want to happen.
```
<div id="root"></div>

function Title() (
    return (
        <section id="welcome">
            <h1>Welcome to Our Page</h1>
        </section>
    )
);
React.DOM.render(<Title />, documentgetElementById("root")
```
