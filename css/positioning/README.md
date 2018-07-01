* https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/1
* https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/2
* https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/3

* [CSS POSITIONING (PART1) - DevTips - 3 Feb 2014](https://www.youtube.com/watch?v=kejG8G0dr5U&list=PLqGj3iMvMa4L731ispRfGAabXeRpM4RL6)
* [CSS POSITIONING (PART 2) - DevTips - 3 Feb 2014](https://www.youtube.com/watch?v=Rf6zAP4YnZA&list=PLqGj3iMvMa4L731ispRfGAabXeRpM4RL6&index=2)
* [Introduction to CSS by Scott Allen - 5: Layout with CSS - Position - 2m 20s](https://app.pluralsight.com/player?course=css-intro&author=scott-allen&name=css-layout&clip=1&mode=live)
  * I guess a when you apply `position: relative;` to an element without the `top: somehting px;` and `left: something px` the elemenis still in static position. 

---
 
- [Sitepoint | Getting Started with CSS By Russ Weakley - Lesson 7, Step 5: Three Key Differences - 4m 48s](https://www.sitepoint.com/premium/courses/getting-started-with-css-2903/lesson/7/step/5) 

#### First Key Difference

What happens to the content that comes after the positioned element?

Absolute: content after the positioned element will ignore the positioned element and will move up underneath it.

Relative: content after the positoned element will leave space for the positioned element.

Fixed: Content after the positioned element will ignore the positional element and will move up underneath it.

#### Second Key Difference 

Do positioned elements shrink-wrap or stay at the same width?

Absolute: Initially shrinks-wrapped but can be sized or stretched.

Relative: If it's a block level element they will initially be streched but they can be given size. If it's a inline element they will initially shrink-wrap and cannot be given size.

Fixed: Initially shrink-wrapped but can be sized or stretched.
