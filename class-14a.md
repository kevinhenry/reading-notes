# Read: 14a - CSS Transforms, Transitions, and Animations

[CSS Transforms Article](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

## Transform Syntax
The transform property followed by the value. Specifies the transform type followed by a specific amount inside parentheses

```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

## 2D Transforms
- Two-dimensional transforms work on the x and y axis, known as horizontal and vertical axis
- Three-dimensional transforms work on both the x and y axis, as well as the z axis

## 2D Rotate - rotate an element from 0 to 360 degrees

HTML
```
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

CSS
```
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

## 2D Scale
Allows you to change the appeared size of an element

HTML
```
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

CSS
```
.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}
```

## 2D Translate
Using the `translateX` value will change the position of an element on the horizontal axis while using the `translateY` value will change the position of an element on the vertical axis

## 2D Skew - used to distort elements on the horizontal axis, vertical axis, or both

## Combining Transforms
It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. In this event multiple transforms can be combined together

## Transform Origin
The dead center of an element, both 50% horizontally and 50% vertically

## Perspective
- In order for three-dimensional transforms to work the elements need a perspective from which to transform
- The perspective of an element can be set in two different ways, one way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed

## Perspective Depth Value
Can be set as none or a length measurement. The none value turns off any perspective, while the length value will set the depth of the perspective

## Perspective Origin
Used for the transform-origin property may also be used with the perspective-origin property, and maintain the same relationship to the element

## 3D Transforms
Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width

## 3D Rotate
Using three-dimensional transforms we can rotate an element around any axis; to do so, we use three new `transform values`, including `rotateX`, `rotateY`, and `rotateZ`

## 3D Scale
By using the `scaleZ` three-dimensional transform elements may be scaled on the z axis

## 3D Translate
Using the `translateZ` value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element.

## 3D Skew - the one two-dimensional transform that cannot be transformed on a three-dimensional scale
Elements may be skewed on the x and y axis, then transformed three-dimensionally as wished, but they cannot be skewed on the z axis Transform Style

## Backface Visibility - when working with three-dimensional transforms, elements will occasionally be transformed in a way that causes them to face away from the screen. This may be caused by setting the rotateY(180deg) value 
 

# Transitions & Animations
[Transitions & Animations Article](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

## Transitions
For a transition to take place, an element must have a change in state, and different styles must be identified for each state
- Transitional Property - determines exactly what properties will be altered in conjunction with the other transitional properties
- Shorthand Transitions
  - Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay
  - Do not use commas with these values unless you are identifying numerous transitions

## Animations
Customizing Animations - provide the ability to further customize an element’s behavior, including the ability to declare the number of times an animation runs, as well as the direction in which an animation completes 


## 8 Simple CSS3 Transitions That Will WOW Your Users Article
[8 Simple CSS3 Transitions That Will WOW Your Users Article](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

CSS3 has introduced countless possibilities for UX designers, and the best thing about them is that the coolest parts are really simple to implement.

- Fade In 
```
.fade
{ 
  opacity:0.5;
}
.fade:hover
{ 
  opacity:1;
}
```

- Change Color 
```
.color:hover
{ 
  background:#53a7ea;
}
```

- Grow & Shrink
```
.grow:hover
{
  -webkit-transform: scale(1.3);
  -ms-transform: scale(1.3);
  transform: scale(1.3);
}
```

- Rotate elements
```
.rotate:hover
{
  -webkit-transform: rotateZ(-30deg);
  -ms-transform: rotateZ(-30deg);
  transform: rotateZ(-30deg);
}
```

- Square to circle
```
.circle:hover
{
  border-radius:50%;
}
```

- 3D shadow
```
.threed:hover
{
  box-shadow:
    1px 1px #53a7ea
    2px 2px #53a7ea
    3px 3px #53a7ea
  -webkit-transform: translateX(-3px);
  transform: translateX(-3px);
}
```

- Swing Reference
- Inset border
```
.border:hover
{
  box-shadow: inset 0 0 0 25px #53a7ea;
}
```
 

[6 Buttons Animated CodePen](https://codepen.io/retyui/pen/ByoaXV)

[CSS3 KeyFrames Animation CodePen](https://codepen.io/akshaychauhan/pen/oAfae)

[404 CodePen](https://codepen.io/kieranfivestars/pen/MYdQxX)

[Pure CSS Bounce Animation CodePen](https://codepen.io/dp_lewis/pen/gCfBv)
