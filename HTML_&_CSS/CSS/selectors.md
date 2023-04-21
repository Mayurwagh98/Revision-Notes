1. CSS selectors are patterns that are used to select and style HTML elements. 
2. Selectors specify which elements on a web page should be affected by a particular style rule.
3. By using selectors, you can apply styles to specific elements or groups of elements on a web page.
4. Tag selectors: Select elements based on their HTML tag name. For example, the following rule will apply to all h1 elements on a page:
```
h1 {
  font-size: 24px;
}
```
5. Class selectors: Select elements based on their class attribute value. For example, the following rule will apply to all elements with the class name "highlighted":
```
.highlighted {
  background-color: yellow;
}
```
6. ID selectors: Select elements based on their ID attribute value. IDs should be unique on a page, so this selector is used to target a specific element. For example, the following rule will apply to the element with the ID "header":
```
#header {
  border-bottom: 1px solid black;
}
```
7. Attribute selectors: Select elements based on the presence or value of their HTML attributes. For example, the following rule will apply to all a elements with the target attribute set to _blank:
```
a[target="_blank"] {
  color: blue;
}
```
8. Pseudo-class selectors: Select elements based on their state, such as whether they are being hovered over or are in a certain position in the document. For example, the following rule will apply to all a elements that are being hovered over by the user:
```
a:hover {
  text-decoration: underline;
}
```
