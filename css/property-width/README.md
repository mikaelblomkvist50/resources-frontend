## Example 1

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">
    <title>Understanding width property in css</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <p>I am a paragraph element and my parent is the body element.</p>

    <div>
      <p>I am a paragrpah element and my parent is the div element and my grand parent is the body element.</p>
    </div>
  </body>
</html>
```

```css
/* For the width of the paragrpah tag it should be 50%, the important question to ask is 50% of what?
   50% of essentially the parent. So in this case the first paragrah tag is 50% of the view port itself.

   Where as the paragraph nested inside of the div tag is 50% of the div tag width which is 50% itself.
   So 50% of 50% is 25%. With margin auto on the sides centers it nicely.
*/

p {
  background: pink;
  width: 50%;
}

div {
  background: yellow;
  width: 50%;
}

div > p {
  margin: 0 auto;
}
```

## Example 2

[CSS Tutorial For Beginners 42 - Width & Height - The Net Ninja - Published on 9 Jul 2015](https://www.youtube.com/watch?v=b9lWNg8lwW4)

```html
<!DOCTYPE html>
```


```css
#main-content div {

}
```
