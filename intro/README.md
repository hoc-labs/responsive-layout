# Responsive Layout

## Percentages vs Fixed-width 

By default, a web page is responsive. A block element will fill 100% of its parent element and text will wrap. Setting fixed widths creates problems for responsive design.

View index.html in the browser with the responsive view enabled in the dev tools and see how the parent and child elements respond to changes in the width.

### Issues with Fixed Widths
Set the width of the parent element to a fixed width.
```css
.parent {
  ...
  width:900px;
}
```
Reduce the screen width. As you can see, the fixed-width is causing horizontal scrolling to activate when the screen width is less than the fixed width of the parent element.

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-1.png)

### Percentage Widths
Set the width of the parent element to be a percetage. 
```css
.parent {
  ...
  width:80%;
}
```
Now the parent element is responsive to the change in the size of the overall window.

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-2.png)


### Issues with Fixed Width/Height on Child Element

```css
.child {
  ...
  width:600px;
}
```
The child element will overflow the parent element when the width exceeds the available window width.

The default behavior is for the content to overflow so that information is not lost, but it requires scrolling to see it.

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-4.png)

Setting a fixed-height causes the same issue as setting a fixed width. Notice as you decrease the width of the container, the content will overflow in the vertical direction.

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-3.png)

### Use max-width to limit text width
Typographers recommend that a paragraph have a width of around 75 characters or 600px (1 character ~ 8 pixels) for legibility reasons. Anything longer than that becomes difficult to read and causes unnecessary strain on the eyes because of the distance the eye has to travel left-to-right and back again.

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-5.png)

![](https://raw.githubusercontent.com/hoc-labs/images/main/responsive-intro-6.png)
### Percentages are Relative to Parent Element Width
Change the width of the child element to be a percentage of the parent element.

```css
.child {
  ...
  width:50%;
}
```
The child content will always fill 50% of the parent element's width.
