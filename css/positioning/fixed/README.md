# When I hear this element is `positioned: fixed;` I think of these things:

1. What happens to the content that comes after the `{ position: fixed; }` element?

Content after the `{ postition: fixed; }` element will ignore the `{ position: fixed; }` element and will move up underneath it. This results in the `{postition: fixed; }` element being overlayed on top of the previously below element which just moved up.

2. Do `{ position: fixed; }` elements shrink-wrap or stay at the same length?

It originally shrink-wraps but can be sized (meaning given `{ width: xxx px; }` or `{ height: xxx px; }`) and strethced (meaning `{ left xxx px; }` and `{ right: xxx px; }` or `{ top: xxx px; }` and `{ bottom: xxx px; }`.)

3. What is the  `{ positioned: fixed; }` element relative to?

It is positioned relative to to the viewport/browser window.

4. What happens if I scroll?

The `{ position: fixed; }` element will sit exactly in the spot where you positioned it when you scroll the browser window. 

---

- [Pluralsight | Introduction to CSS by Scott Allen - 5: Layout with CSS - Absolute and Fixed Positioning - 1m 28s](https://app.pluralsight.com/player?course=css-intro&author=scott-allen&name=css-layout&clip=3&mode=live)

---

- [Pluralsight | CSS Positioning by Susan Simkins - 2: CSS Positioning - Fixed Positioning - 7m 32s](https://app.pluralsight.com/player?course=css-positioning-1834&author=susan-simkins&name=css-positioning-1834-m2&clip=0&mode=live)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Positioning Fixed</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="box blueBox"></div>
    <div class="box greenBox"></div>
    <h1>Understanding CSS Positioning</h1>
    <p><em>Fixed positioning</em> &rsquo;fixes&lsquo; the position of an element relative to the browser window. The element always stays fixed in place, even when scrolling.</p> 
  </body>
</html>
```

```css
body {
  background-color: #1f1f1f;
  color: #bfbfbf;
}

h1 { font-weight: normal; }

em { color: #e07a05; }

.box {
  width: 100px;
  height: 100px;
  margin-bottom: 10px;
}

.blueBox {
  background: #627da0;
}

.greenBox {
  background: #5b8054;
}

/* add the property */
.blueBox {
  position: fixed;
}

/* understanding values */
.blueBox {
  top: 150px;
/*  bottom: 150px;*/
  left: 150px;
/*  right: 25px;*/
}
/* You can't have two conflicting values on each axis.
   So if you think of it like a graph you can only have
   one value from the top to bottom.
   Or one value horizontally from left to right.
*/

/* Another key thing to understand fixed positioning is
   where it stays relative to the browser window.
   To see what I mean by this I'm going to apply a height
   to the body to get a scroll bar that moves our page */
body {
  height: 2000px;
}
/* As we move the scroll bar, you can see what
   fixed positioning actually does. And it's fixing it
   in place realtive to the browser window. */
```
---

- [Sitepoint | Getting Started with CSS By Russ Weakley - Lesson 7, Step 4: Fixed Positioning - 5m 15s](https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/4) 

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Lesson 07: Exercise 01 - fixed positioning - start</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="container">
      <h1>Lesson 07: Exercise 01 - fixed positioning - start</h1>
      <p>Lorem ipsum dolor sit amet consect etuer adipi scing elit sed diam nonummy nibh euismod tinunt ut laoreet dolore magna aliquam erat volut. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.</p>
      <h2>Heading level 2</h2>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
      <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
      <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
       <p>Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.</p>
       <p>Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.</p>
    </div>
  </body>
</html>
```

```css
body {
  margin: 0;
  padding: 20px;
  font-size: 100%;
}

h1 { margin: 0 0 .5em; }

h2 {
  margin: 0;
  border: 1px solid red;
  background: yellow;
}

.container {
  width: 50em;
  margin: 0 auto;
  border: 1px solid blue;
}

/* add the property */
h2 { position: fixed; }
/* As soon as we set this to postion fixed the content below shifted up
   because the h2 element has moved off the page. The other thing that has
   happend is that this element has shrink wraped. It was a block level element
   and now it's shriked wraped in around the content (it still is display: block;)
   though.
   The key question is what is this element being positioned against??? */

/* understanding values */
h2 { left: 20px; }
/* It's positioned it self 20px away from the left edge of the view port.
   If you scrool up then down you can see how interesting this element is.
   It remains fixed in place relative to the viewport. */
h2 { top: 40px; }

/* stretched */
h2 {
  left: 0;
  right: 0;
}

/* sized */
h2 { width: 300px; }
```

---

[You Tube | CSS POSITIONING (PART 2) - DevTips - 3 Feb 2014 - 10m 49s](https://www.youtube.com/watch?v=Rf6zAP4YnZA&index=2&list=PLqGj3iMvMa4L731ispRfGAabXeRpM4RL6) 

Before the tutorial:

`index.html`:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Positioning Absolute</title>
    <link href="style.css" rel="stylesheet">
  </head>
  <body>
    <div class="grand-dad">
      <div class="dad">
        Ut in nulla enim. Phasellus molestie non est bibendum non <span class="me">venenatis</span> nisl tempor. Suspendisse dictum feugiat nisl ut dapibus. Mauris iaculis porttitor posuere. Praesent id metus massa, ut blandit odio. Proin quis tortor.
      </div>
    </div>
  </body>
</html>
```

`style.css`:
```css
body {
  font-family: sans-serif;
  padding: 100px;
}

.me {
  background: pink;
}
```
