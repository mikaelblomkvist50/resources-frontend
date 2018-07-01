[You Tube | CSS Animation Tutorial #2 - Transforms - The Net Ninja - 12 Apr 2016 - 10m 19s](https://www.youtube.com/watch?v=PH35-BDak0M&t=) 

Before the tutorial:

`index.html`:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Transform</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="wrapper">
      <img src="cloud.png">
    </div>
  </body>
</html>
```

`style.css`:
```css
body {
  background: lightblue;
  text-align: center;
}

.wrapper {
  width: 100%;
  padding: 20px;
  box-sizing: border-box;
}

img {
  transform: translate(-300px, 600px)
}
/* 
trnslate just means move the element from one positino to another on the web page.
So if I want to translate it across to the right I can use translate x.
If I want to move it along the y-axis I can use translate y.

If you just put one value in, it will just translate it on the x-axis.
*/
```
