# CSS

**Cascading Style Sheets**

[HTML Cheatsheet](https://htmlcheatsheet.com/) Includes properties, selectors, background generator, button generator etc...

## Floats & Clears

```CSS
img {
  float: left;
  margin-right: 20px // optional
}
```

ex. you have a paragraph after an image, using `float:left` the text wraps on the right side of the image.

float brings items up in the air and lets other things go underneath it other than text.

```CSS
p {
  clear: both;
}
```

using `clear: both` the p element takes up all the space and starts after the img. text wont go underneath because it will pretend the item above isn't float and will start on the next line.

ex. you have 2 boxes you want next to eachother. use `float:left` on left box and `float:right` on right box. they will be next to eachother if there is enough space.

If first element is floating left, it is possible that the second block is beneath the floating one. Solve this by adding the float property left to the second block to have no overlap between the two blocks.

![Floats](../images/CSS/float.png)

By doing this the third box is having the same problem as the scond one. it is now beneath the first box.

If you add float left to all the boxes there will be a horizontal line that wraps around on the next line if the screen width gets narrow.

note: when floating right it will reverse the order. completely right is box 1.

`clear:both` forces a new line. ignore the things that are floating above it and instead come down on the next line.

`clear:right` only pays attention to items floating to the right. if there are none nothing happens. Same with `clear:left`

## Positioning

### Static Positioning

Is default position all elements will have. Static makes it so elements are shown in chronological order.

ex. child element one will be above child element two.

### Relative Position

Acts exactly as static positioning but it allows you to do 4 specific things that static does not.

It allows you to change the `top, left, right, bottom`. It takes the element out of the document flow and moves it in the specified direction.

### Absolute Position

completely removes the element from the document flow and everything else renders as if the absolute element doesn't exist

![absolute positioning](../images/CSS/absoluteposition.png)

Usefull when you want to stick an element in a specific position but you don't want anything else moving around because of it.

When using the top, left, bottom, right properties they are now calculated from the parent element. To make a parent set `position:relative`. The child element will stick to any parent that's not static.

### Fixed Position

These elements are positioned based on the entire HTML element. They also stay in place when you scroll.

### Sticky Position

Combination of both relative position and fixed position. Positions itself relative to other elements but when scrolled down it will become fixed and stay in the same place.

## Display

Default display property is `display:block` which means it will take up the entire width given to it. All the content has to be above it or below it.

![Markdown Logo](../images/CSS/display.PNG)

**RED & GREEN** => `display:block` takes up entire width

**CYAN** => `display:inline` takes up the minimum needed space to fit content.

**IMAGE** => `display:inline-block` takes up the minimum needed space to fit content. using this display property allows you to set the `width` & `height` of the element.

`display:none` makes the element disapear, takes up no space.

`display:flex` more on that later in the document

`display:grid` more on that later in the document

## Box Model

**Everything in CSS is a box of either a rectangular shape or a square shape**


![Margin padding](../images/CSS/marginpadding.PNG)

**Margin collapses between two elements that are next to eachother.**

- Whatever margin is largest is the one that will be used.
- Margin doesn't count in to the actual height of an element.
- To include the margin into the actual height of an element use `box-sizing:border-box` this subtracts the padding and the margin from the content. so that the original defined `height` & `width` is the size the box takes.

Good way to learn more about the box model is playing around in the chrome dev tools.

It is easier to use `box-sizing:border-box` because you won't have to do math in your head and the box will stay the origionally indented size.

## Flex Box

`display:flex` allows the boxes to line up next to eachother and take up the `width` if there is space. if the screen gets to small the boxes will shrink. To position the boxes on the `Main Axis` use `justify-content`. To position the content on the `Main Axis` use `align-items`. The property `align-content` property should be used for multi-line flex box containers. This in combination with `flex-wrap` on the container makes the items shift to different lines to keep the same `width`

Properties justify-content:
- `center`
- `space-between`
- `space-around` even space around all flex items
- ``

Properties align-items:
- `stretch` default property, take up the most possible space
- `flex-start` takes up the intended size
- `center` align items on the main axis with the intended size
- `` 

![Flex Box](../images/CSS/flexbox.PNG)

## CSS Grid

![CSS Grid](../images/CSS/CSSGrids.PNG)







