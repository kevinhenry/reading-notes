# Read: 03 - HTML Lists, CSS Boxes, JS Control Flow

## HTML Book by Jon Duckett
<h1>Introduction</h1>

## Chapter 3: “Lists” (pp.62-73)

HTML has three types of lists:

Ordered lists `<ol></ol>` have items listed sequentially and *numbered*.

Unordered Lists `<ul></ul>` beginning with a *bullet* point instead of a character to indicate order.

Definition lists `<dl></dl>/` are made of of a set of terms along with the *definitions for each of those terms*. Inside the `<dl>` element you will usually see pairs of `<dt>` and `<dd>` elements.

  `<dt>` is used to contain the term being defined (definition term).
  `<dd>` is used to contain the definition.

  ...
  <dl>
    <dt>Sashimi</dt>
    <dd>Sliced raw fish</dd>
    <dt>Scale</dt>
    <dd>A technique</dd>
    <dt>Scamorze</dt>
    <dt>Scamorzo</dt>
    <dd>An Italian cheese</dd>
  </dl>
  ...

Nested List can be used to put a second list inside an `<li>` element to create a sub-list or nested list. They will be displayed indented further than the parent list.

...
<ul>
  <li>Mousses</l1>
  <li>Pastries
    <ul>
      <li>Croissant</li>
      <li>Mille-feuille</li>
    </ul>
  </li>
  <li>Tarts</li>
</ul>
...


## Chapter 13: “Boxes” (pp.300-329)

CSS treats each HTML element as if it lives in its own box. By default the box size is just enough to hold its contents.

### Box Dimensions:

Width, height - allow the specification of the size of the box. Most popular methods are to use, pixels, percentages, or ems.

Pixels `px` tend to be most popular because they allow designers to accurately control the size.

Percentages `##%` end up with the box relative to the size of the browser window, or in the case that it is inside of a box, it is a percentage of the containing box.

EMS `em` - the size of the box is based on the size of the text within it.

### Limiting Width:

`min-width` - property specifies the smallest size a box can be displayed at when the browser window is narrow

`max-width` - property indicates the maximum width a box can stretch to when the browser window is wide.

Limiting Height: In the same way that the width of a box on a page is limited, the height can be limited. This is achieved with `min-height` and `max-height` properties.

### Overflowing Content:

Overflow - property tells the browser what to do if content contained within the box is larger than the box itself. The overflow property is handy because some browsers allow users to adjust the size of the text to appear as large or as small as they want. If the text is too large, the page can become unreadable. Hiding the overflow prevents items overlapping on the page. It can have one or two values:

`hidden` - property hides any extra context that does not fit in the box.

`scroll` - property adds a scrollbar to the box so that it can scroll to see the missing contents.

Every box has three properties that can be adjusted to control its appearance.

`border` - Every box has a border. The border separates the edge of one box from another.


`margin` - Sits outside the edge of the border. Width of the margin can be set to create a gap between the borders of two adjacent boxes.


`padding` - The space between the border pf a box and any content contained within it. Adding padding can increase the readability of the contents.

### White Space & Vertical Margin

The padding and margin properties help by adding space between various items on the page.

White Space - the space between two items on a page.

`border-width` - used to control the width of a border. Value can either be given in pixels or one of the following values:

`thin`
`medium`
`thick`

You cannot use percentages with border-width.

You can control the individual size of boarders using four seperate properties:

`border-top-width`
`border-right-width`
`border-bottom-width`
`border-left-width`

You can also specify different widths for the four border values in one property:

`border-width: 2px 1px 1px 2px;`

The values flow in a clockwise order: top, right, bottom, left.

### Border Style

`border-style` - controls the style of a border. The property can take the following values:

`solid` - single solid line
`dotted` - a series of square dots
`dashed` - series of short lines
`double` - two solid lines (the value of the border-width property creates the sum of the two lines)
`groove` - appears to be carved into the page
`ridge` - appears to stick out from the page
`inset` - apprears to be embedded into the page
`outset` - appears to be coming out of the screen
`hidden/none` - no border is shown

You can individually change the styles of different boarders using:
`border-top-style`
`border-left-style`
`border-right-style`
`border-bottom-style`

### Border Color

`border-color` - you can specify the color of a border using RGB, HEX, or CSS color names (REF p251-252)

It is possible to control the colors of individual sides of a border using:

`border-top-color`
`border-right-color`
`border-bottom-color`
`border-left-color`

It is also possible to used shorthand to control all four border colors in one property:

`border-color: darkcyan deeppink darkcyan deeppink;`

The values appear in a clockwise order: top, right, bottom, left.


### Shorthand

`border` - property allows the specification of width, style and color of a boarder in one property. Values should be coded in that specific order:

...
p {
  width: 250px;
  border: 3px dotted #0088dd;}
...

### Padding

`padding` - property allows the specification of how much space should appear between the content of and element and its border.

`padding-top`
`padding-right`
`padding-bottom`
`padding-left`

### Margin

`margin` - controls the gap between boxes. Commonly given in pixels. Can use percentages or ems.

`margin-top`
`margin-right`
`margin-bottom`
`margin-left`

### Centering Content

If you want to center a box on the page or center it inside the element that it sits in, you can set `left-margin` and `right-margin` to auto.

### Change Inline/Block

`display` - allows you to turn an inline element into a block-level element and vice versa. It can also be used to hide an element from the page.

`inline`

`block`

`inline-block`

`none`

### Hiding Boxes

`visibility:` - allows you to hide boxes from users, but leaves a space where the element would have been.

`hidden`

`visible`

* * *

## JS Book by Jon Duckett
<h1>Introduction</h1>

Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)

## Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

### If...Else Statements

The if...else statement checks a condition. If it resolves to true the first code block is executed. If the condition resolves to false the second code block is run instead.

If...else statements allow you to provide two sets of code:

1. one set if the condition evaluates to true
2. another set if the condition is false

### Switch Statements

A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that values.

### Truthy & Falsy Values

Due to type coercion, every value in JavaScript can be treated as if it were true or false; and this has some interesting side effects.

Falsy values are treated as if they are false. Falsy values can also be treated as the number 0.

Truthy values are treated as if they are true. Almost everything that is not in the falsy able can be treated as if it were true. Truthy valuers can also be treated as the number 1.

### Loops

Loops check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns fase. There are three common types of loops:

For - Run code for a specific number of times

While - Will run while a condition is true

Do While - Will always run the statements inside the curly brace at least once, even if the condition evaluates to false.

### Loop Counters

A for loop uses a counter as a condition. This instructs the code to run a specified number of times.
