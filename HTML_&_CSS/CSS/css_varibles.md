1. CSS variables, also known as CSS custom properties, are a type of variable that can be used to store and reuse values in CSS stylesheets. CSS variables are defined using the -- prefix, followed by a name and a value.
```
:root {
  --main-color: #006699;
}

h1 {
  color: var(--main-color);
}
```
2. In the above example, we define a CSS variable --main-color with a value of #006699. The :root selector is used to define the variable globally for the entire document. The variable is then used in the h1 selector to set the color of the h1 element to the value of the --main-color variable.
3. CSS variables can also be used to create dynamic styles that respond to changes in the viewport or user interactions. For example, you could define a variable for the width of a sidebar and then use that variable in your layout styles, like this:
```
:root {
  --sidebar-width: 200px;
}

.sidebar {
  width: var(--sidebar-width);
}

.content {
  margin-left: var(--sidebar-width);
}
```
4. In this example, the --sidebar-width variable is used to define the width of the sidebar. The variable is then used in the styles for the .sidebar and .content elements to ensure that the content is properly laid out around the sidebar.
