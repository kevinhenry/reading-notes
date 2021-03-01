# Read 12 - Chart.js and Canvas

## HTML Book by Jon Duckett
<h1>Introduction (2-11)</h1>

Chart.js API Article

Chart.js is a JavaScript plugin that uses HTML5's canvas elements to draw graphs onto pages

It can make bar charts, line charts, pie charts and more

Adding Charts takes 3 steps:

  - Adding Canvas element
  - Retrieving the element to create the graph
  - give the chart data

Canvas element will have an open and closed `<canvas>` tag

Script tag will involve the following for types of charts

  `new Chart().Line();`
  `new Chart().Pie();`
  `new Chart().Bar();`

## Canvas API
Canvas tag doesn't hav a src or alt like imgs but could use width and height. These are optional and if none are specified the default is 300px wide and 150px high

When rendering, the script uses method called `getContext()`. It takes one parameter for the type of context -- for 2D you'd use `'2d'`

## Drawing Shapes
Grid - is our space that we designate using the width and height. 1px corresponds to 1 unit on the grid

## Rectangles
There are 3 functions that draw rectangles:
`fillRect(x, y, width, height)` - draws a filled rectangle
`strokeRect(x, y, width, height)` - draws a rectangular outline
`clearRect(x, y, width, height)` - clears the rect..making it transparent

## Paths
- A Path is a list of points, connected by segments. Can be different shapes, curved or not
- You can use paths to make shapes like triangles

## Path Functions
`beginPath()` - creates a new path
`closePath()` - adds a straight line to the path
`stroke()` - draws the shape by stroking its outline
`fill()` - draws a solid shape by filling in content area
`moveTo(x,y)` - moves the pen to new coordinates, doesn't draw anything

## Lines
Straight lines use `lineTo(x,y)` method

## Colors
`fillStyle = color` - sets the style used when filling in shapes
`strokeStyle = color` - sets the style for shapes outlines

## Line Styles
`lineWidth = value` - Sets the width of lines drawn in the future.
`lineCap = type` - Sets the appearance of the ends of lines.
`lineJoin = type` - Sets the appearance of the "corners" where lines meet.
`miterLimit = value` - Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
`getLineDash()` - Returns the current line dash pattern array containing an even number of non-negative numbers.
`setLineDash(segments)` - Sets the current line dash pattern.
`lineDashOffset = value` - Specifies where to start a dash array on a line.

## Text
2 methods for rendering text
`fillText(text, x, y [, maxWidth])` - fills a given text at x,y position
`strokeText(text, x, y [, maxWidth])` - strokes a given text at the give x,y position
