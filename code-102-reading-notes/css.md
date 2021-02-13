# Color
The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways:
1. **rgb values**

These express colors in terms
of how much red, green and
blue are used to make it up. For
example: rgb(100,100,90)

2. **hex codes**
These are six-digit codes that
represent the amount of red,
green and blue in a color,
preceded by a pound or hash #
sign. For example: #ee3e80

3. **color names**
There are 147 predefined color
names that are recognized
by browsers.

**EXAPMLE**

/* color name */

h1 {

color: DarkCyan;}

/* hex code */

h2 {

color: #ee3e80;}

/* rgb value */

p {

color: rgb(100,100,90);}

## Background Color
CSS treats each HTML element
as if it appears in a box, and the
background-color property
sets the color of the background
for that box.
You can specify your choice of
background color in the same
three ways you can specify
foreground colors: RGB values,
hex codes, and color names
(covered on the next page).

**EXAMPLE**

body {

background-color: rgb(200,200,200);}

h1 {

background-color: DarkCyan;}

h2 {

background-color: #ee3e80;}

p {

background-color: white;}


***Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker.***



### Opacity
CSS3 introduces the opacity
property which allows you to
specify the opacity of an element
and any of its child elements.
The value is a number between
0.0 and 1.0 (so a value of 0.5
is 50% opacity and 0.15 is 15%
opacity).

### Hsl AND Hsla
The hsl color property has
been introduced in CSS3 as an
alternative way to specify colors.
The value of the property starts
with the letters hsl, followed
by individual values inside
parentheses for:
hue
This is expressed as an angle
(between 0 and 360 degrees).
saturation
This is expressed as a
percentage.
lightness
This is expressed as a
percentage with 0% being white,
50% being normal, and 100%
being black.

**SKIMMED**
* It is important to ensure that there is enough contrast
between any text and the background color (otherwise
people will not be able to read your content).

* CSS3 has introduced an extra value for RGB colors to
indicate opacity. It is known as RGBA.

* CSS3 also allows you to specify colors as HSL values,
with an optional opacity value. It is known as HSLA
