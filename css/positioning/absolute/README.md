When I hear this element is `position: absolute;` I think of these things:

1. What happens to the content that comes after the `{ position: absolute; }` element?

Content after the `{ position: absolute; }` element will ignore the `{ position: absolute; }` element and will move up underneath it. This results in the `{ position: absolute; }` element being overlayed on top of the previously below element which just moved up.

2. Do `{ position: absolute; }` elements shrink-wrap or stay at the same length?

It originally shrink-wraps but can be sized (meaning given `{ width: xxx px; }` or `{ height: xxx px; }`) and stretched (meaning `{ left: xxx px; }` and `{ right: xxx px; }` or `{ top: xxx px; }` and `{ bottom: xxx px; }`.)

3. What is the  `{ position: absolute; }` element relative to?

It is positioned relative to the nearest ancestor with postioning meaning an ancestor that has `{ position: realtive; }`. However if no ancestors has `{ position: relative; }` then the element `{ postion: absolute; }` will be postioned realtive to the viewport/browser window.


- [Sitepoint | Getting Started with CSS By Russ Weakley - Lesson 7, Step 2: Absolute  Positioning - 8m 15s](https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/2) 

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Lesson 07: Exercise 01 - absolute positioning - start</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
  <div class="container">
    <h1>Lesson 07: Exercise 01 - absolute positioning - start</h1>
    <p>Lorem ipsum dolor sit amet consect etuer adipi scing elit sed diam nonummy nibh euismod tinunt ut laoreet dolore magna aliquam erat volut. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.</p>
    <h2>Heading level 2</h2>
    <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
    <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```

```css
body
{
  margin: 0;
  padding: 20px;
  font-size: 100%;
}

h1 { margin: 0 0 .5em; }

h2 {
  margin: 0;
  border: 1px solid red;
  background: rgba(255,255,0,.5);
}

.container {
  width: 50em;
  margin: 0 auto;
  border: 1px solid blue;
}

/* add the property */
h2 { position: absolute; } 
/* Great example of becoming out of normal flow.
   And the content blow that is in flow has moved up.
   Ignoring the out of normal flow h2 content. */
   

/* positioned against? */
h2 {
  left: 0;
  top: 0;
}
/* This makes the h2 jump to the top of the page
   Why did that happen??? 
   Well it's looking for a parent element with positioning.
   And if it can't find any it will then position it self relative to the view port.
   But isn't the h2 elements parent the .container class???
   That's right however the .container class doesn't have positioning so it chose
   the view port.
   If we give the the .container class some positioning then h2 will position
   it self relative to the .container class. */

.container {
  position: relative; 
}

/* understanding values */
h2 { left: -20px; }
h2 { top: 40px; }

/* stretched */
h2 {
  left: 0;
  right: 0;
}

/* sized */
h2 { width: 300px; }
```
