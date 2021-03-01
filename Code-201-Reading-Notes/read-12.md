# Charts
charts its for displaying data in easer way than tables we have here 3 type of graphs3

+ line chart
+ pie char
+ bar chart

we put the link of javascript on htmal which src will be chart.min.js `<script src='Chart.min.js'></script>` and in footer write a script that will retrieve the context of the canvas and we will follow the steps of coding

`<canvas>` its look like img but it has only two attributes, width and height and it have a closing tags `</canvas>` When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high and we can give it an id and styling like any element


# The rendering context
The `<canvas>` element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics

`<canvas id="my-house" width="300" height="300"></canvas>`
const canvas = document.getElementById('my-house');
const ctx = canvas.getContext('2d');
Drawing shapes with canvas
`<canvas>` only supports two primitive shapes rectangles and paths and There are three functions that draw rectangles on the canvas


- rectangle with these different type of function
1. fillRect(x, y, width, height)
2. strokeRect(x, y, width, height)
3. clearRect(x, y, width, height):making it fully transparent

- drawing paths
1. beginPath() it's a function
2. closePath() : adds a straight line to the path
3. stroke()
4. fill()

+ moveTo(x, y) function can helping you in moving the pen
+ lines by lineTo(x, y)method
+ arc we use the arc() or arcTo() methods ==arcTo(x1, y1, x2, y2, radius)
+ bezier and quadratic curves by quadraticCurveTo(cp1x, cp1y, x, y)method


# Applying styles and colors
Colors

1. fillStyle = color as string
2. strokeStyle method
Transparency

**globalAlpha = transparencyValue or you can add it into rgb color**

Line styles


- lineWidth = value
- lineCap = type
- lineJoin = type
- miterLimit = value
- getLineDash()
- setLineDash(segments)
- lineDashOffset = value

 **Gradients with this methods**

- createLinearGradient(x1, y1, x2, y2)

- createRadialGradient(x1, y1, r1, x2, y2, r2)

- createConicGradient(angle, x, y)

gradient.addColorStop(position, color) then added it to fillStyle or strokeStyle properties

Patterns by createPattern(image, type)

1. repeat

2. repeat-x

3. repeat-y

4. no-repeat

`var ptrn = ctx.createPattern(img, 'repeat');`

**Shadows**

shadowOffsetX = float

shadowOffsetY = float

shadowBlur = float

shadowColor = color

**Drawing text**

there two methods to render text

1. fillText(text, x, y [, maxWidth])
2. strokeText(text, x, y [, maxWidth])
3. Styling text by this property

font = value

textAlign = value

textBaseline = value

direction = value