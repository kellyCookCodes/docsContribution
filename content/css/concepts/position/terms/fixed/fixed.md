---
Title: 'fixed'
Description: 'Positions an element relative to the viewport, removing it from the document flow and keeping it fixed during page scrolling.'
Subjects:
  - 'Code Foundations'
  - 'Computer Science'
  - 'Web Design'
  - 'Web Development'
Tags:
  - 'Attributes'
  - 'CSS'
  - 'Design'
  - 'Development'
  - 'Elements'
  - 'Properties'
  - 'Programming'
  - 'Responsive'
  - 'Static Site'
  - 'Style'
  - 'Syntax'
  - 'UI'
  - 'UX'
  - 'Values'
CatalogContent:
  - 'learn-css'
  - 'paths/front-end-engineer-career-path'
  - 'paths/full-stack-engineer-career-path'
---

Positions an [html](https://www.codecademy.com/resources/docs/html) element, removes it from the normal document flow, and pins it to a specified [position](https://www.codecademy.com/resources/docs/css/position); it will remain **fixed** even while scrolling the page.

## Syntax
 ```position: fixed;```

An element with a **fixed** position will be positioned relative to the viewport or the html element. In other words, it is fixed relative to the document it self. 

>**Note**: This differs from [absolute](https://www.codecademy.com/resources/docs/css/position/absolute) positioning which is positioned relative to its closest ancestor/parent element whose position is also set to a value of [relative](https://www.codecademy.com/resources/docs/css/position/relative) or **absolute** (a non-static position).

## Example
 
### HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <meta lang="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fixed Postion</title>
    <link rel="stylesheet" href="style.css" type="text/css">
  </head>
  <body>
    <nav class="fixed">
      <h1 class="content">Hello World!</h1>
    </nav>
  </nav>
  </body>    
</html>
```
In the code block above, the `nav` element is given the class `fixed` in the HTML.

### CSS

```css
html {
  box-sizing: border-box;
  background-color: black;
}

nav.fixed {
  display: inline-block;
  height: 80px;
  width: 100%;
  position: fixed;
  top: 50px;
  left: 100px;
  background-color: white;
  border: 4px solid red;
}
```

In the code block (above) the nav element with the *class of fixed* has its position property set to **fixed** in [CSS](https://www.codecademy.com/resources/docs/css) as well as its **top** and **left** properties with values of 50px and 100px respectively.
This will render in the browser as shown in the image (below).

![Image of a fixed nav element in the browser window/viewport.](https://raw.githubusercontent.com/Codecademy/docs/main/media/position-fixed-example.png)

In the code above, we see that the `nav` element has been taken out of the document flow. As shown in the **CSS** example, the nav element has been moved 50px from the top (moving it down by 50px) and 100px from the left (moving it right by 100px). 

>**Note**: Although the `width` property is set to 100%, the nav element is removed from the normal flow of the document and positioned 100px from the left, which may cause it to extend beyond the right side of the viewport depending on the viewport width and the element's total width (including padding and borders).

 If the `nav` element had the `position` property set to [`static`](https://www.codecademy.com/resources/docs/css/position/static) (the default value), it would remain in its default position, flush against the top-left corner of the viewport.

![Image of a static nav element in the browser window/viewport.](https://raw.githubusercontent.com/Codecademy/docs/main/media/position-static-example.png)
