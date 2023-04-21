1. position: relative: When an element is positioned relatively, it is positioned relative to its normal position on the page. This means that any styles that are applied to the element (such as margins or padding) will still affect the element, even if it is moved using relative positioning.
2. position: absolute: When an element is positioned absolutely, it is positioned relative to its nearest positioned ancestor (i.e. an ancestor that has a position other than static). If there is no positioned ancestor, the element will be positioned relative to the initial containing block (usually the body element). When an element is positioned absolutely, it is taken out of the normal document flow, which means that other elements on the page will not be affected by its position.
```
<div class="parent">
  <div class="child-1"></div>
  <div class="child-2"></div>
</div>

css---
.parent {
  position: relative;
}

.child-1 {
  position: relative;
  top: 50px;
  left: 50px;
  background-color: red;
}

.child-2 {
  position: absolute;
  top: 50px;
  left: 50px;
  background-color: blue;
}
```
3. In this example, the parent element has relative positioning, while child-1 and child-2 both have absolute positioning. child-1 is positioned relative to its normal position within the parent element, while child-2 is positioned relative to the parent element itself. As a result, child-1 is moved down and to the right by 50 pixels, while child-2 is positioned at the top left corner of the parent element.
4. So, to summarize, the main difference between position: absolute and position: relative is that position: absolute takes an element out of the normal document flow and positions it relative to a specified ancestor, while position: relative positions an element relative to its normal position within the document flow.
