## 1. CSS Box Model
Box model describes how elements are rendered and how spacing works on a web page. 
Each element is a box made up of several parts:


content : The actual text, image, or other media inside the element.
```html
<div>Hi!</div>
```

padding : The space between the content and the border. 
It creates an inner space inside the element, making the content not stick to the border.
```css
div {
  padding: 20px;
}
```

border : The line that wraps around the padding and content. 
It separates the content (with padding) from the margin.
```css
div {
  border: 2px solid black;
}
```

margin : The space outside the border. It separates the element from other elements on the page.
```css
div {
  margin: 20px 10px 20px 10px; /*It operates clockwise.*/
}
```