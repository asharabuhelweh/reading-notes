# Images

Images can improve the design and the appearance of a web page.

**Adding Images**

`<img src="img_kid.jpg" alt="kid in a jacket">`

Height & Width
of Images

`<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />`

 Place Images
in Your Code:

1. 1: before a paragraph
The paragraph starts on a new
line after the image.
2. inside the start of a
paragraph
The first row of text aligns with
the bottom of the image.
3. in the middle of a
paragraph
The image is placed between the
words of the paragraph that it
appears in.

**Old Code: Aligning Images Horizontally**

align horizontally.html HTML
The align attribute was
commonly used to indicate how
the other parts of a page should
flow around an image.

The align attribute can take
these horizontal values:

**left**
This aligns the image to the left

**right**
This aligns the image to the right

**Old Code: Aligning Images Vertically**

**top**
This aligns the first line of the
surrounding text with the top of
the image.

**middle**
This aligns the first line of the
surrounding text with the middle
of the image.

**bottom**
This aligns the first line of the
surrounding text with the bottom
of the image.

**Three Rules for Creating Images**

1. Save images in the right format
2. Save images at the right size
3. Use the correct resolution

There are several tools you can use to edit and
save images to ensure that they are the right
size, format, and resolution.
The most popular tool amongst
web professionals is **Adobe Photoshop**

**Image Formats: JPEG**
Whenever you have **many different
colors** in a picture you should use **a JPEG**.


**Image Formats: GIF**
Use GIF or PNG format
when saving images
with few colors or large
areas of the same color.

**Image Dimensions**
The images you use on your website should be
saved at the same width and height that you
want them to appear on the page.

* REDUCING IMAGE SIZE
You can reduce the size of
images to create a smaller
version of the image.

- INCREASING IMAGE SIZE
***You can't increase the size of
photos significantly without
affecting the image quality.***

- CHANGING SHAPE
Only some images can be
cropped without losing valuable
information.


**Cropping Images**
When cropping images it is important not to
lose valuable information. It is best to source
images that are the correct shape if possible.


**Image Resolution**
Images created for the web should be saved at
a resolution of **72 ppi**. The higher the resolution
of the image, the larger the size of the file.

**Vector Images**
 are created by
placing points on a grid, and
drawing lines between those
points. A color can then be
added to "fill in" the lines that
have been created.

The advantage of creating line
drawings in vector format is that
you can **increase the dimensions
of the image without affecting
the quality of it.**

**Transparency**
Creating an image that is partially transparent
(or "see-through") for the web involves selecting one of two formats:
* Transparent GIF
* PNG 


**Checking the Size of Images**
right click on the image of website and open it in a new tab 
it will show under the image the size of image.

**Figure and Figure Caption**
`<figure>`
Images often come with
captions. HTML5 has introduced
a new `<figure>` element to
contain images and their caption
so that the two are associated.

**You can have more than one image inside the `<figure>`
element as long as they all share the same caption.**

The `<figcaption>` element has
been added to HTML5 in order
to allow web page authors to add
a caption to an image.

# Color
Foreground Color


The **color** property allows you
to specify the **color of text inside an element.** 

You can specify any
color in CSS in one of three ways:
1. **rgb values**
These express colors in terms
of how much red, green and
blue are used to make it up. For
example: rgb(100,100,90)

    Values for red, green, and blue
are expressed as numbers
between 0 and 255.

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

**background-color**

CSS treats each HTML element
**as if it appears in a box**, and the
background-color property
sets the color of the background
for that box.

***Every color on a computer screen is created by mixing amounts of red,green, and blue. To find the color you want, you can use a color picker.***



**Hue** is near to the colloquial idea
of color

**Saturation** refers to the amount
of gray in a color. At maximum
saturation, there would be no
gray in the color. At minimum
saturation, the color would be
mostly gray.

**Brightness** (or "value") refers
to how much black is in a color.

**Contrast**

- Low Contrast
Text is harder to read when
there is low contrast between
background and foreground
colors.
- High
Contrast
- Medium contrast 



# Text
Typeface Terminology

change the type of font 

Weight of font 
* Light
* Medium
* Bold
* Black

Style of font 
* Normal
* Italic
* Oblique

Stretch of font 
* Condensed
* Regular
* Extended

Specifying Typefaces

**font-family**

The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.

Size of Type

**font-size**
The font-size property enables
you to specify a size for the
font.
 
 There are several ways to
specify the size of a font:
1. pixels
2. percentages
3. ems

**@font-face** allows you to use
a font, even if it is not installed
on the computer of the person
browsing, by allowing you to
specify a path to a copy of the
font, which will be downloaded if
it is not on the user's machine.

`@font-face {
font-family: 'ChunkFiveRegular';
src: url('fonts/chunkfive.eot');
src: url('fonts/chunkfive.eot?#iefix')
format('embedded-opentype'),`


UpperCase &LowerCase

text-transform

**uppercase** This causes the text to appear
uppercase.

**lowercase**
This causes the text to appear
lowercase.

**capitalize**
This causes the first letter of
each word to appear capitalized.

**text-decoration**
- **none**
This removes any decoration
already applied to the text.

- **underline**
This adds a line underneath the
text.

- **overline**
This adds a line over the top of
the text.

- **line-through**
This adds a line through words.

- **blink**
This animates the text to make it
flash on and off

**line-height**

Leading (pronounced ledding) is
a term typographers use for the
vertical space between lines of
text.

**Letter & Word Spacing**

**letter-spacing**

**word-spacing**


**text-align**:
left , right , center , justify

**vertical-align**

vertical-align: text-top

vertical-align: baseline

vertical-align: text-bottom

**text-indent**
The text-indent property
allows you to indent the first
line of text within an element.

**text-shadow**
take three lengths and a color for
the drop shadow:
1. The first length indicates how
far to the left or right the shadow
should fall.
2. The second value indicates the
distance to the top or bottom
that the shadow should fall.
3. The third value is optional and
specifies the amount of blur that
should be applied to the drop
shadow.
4. The fourth value is the color of
the drop shadow.



**:first-letter, :first-line**
You can specify different values
for the first letter or first line of
text inside an element.

**Styling Links**

**:link**
This allows you to set styles
for links that have not yet been
visited.

**:visited**
This allows you to set styles for
links that have been clicked on.


**Responding to Users**
:hover, :active, :focus

**Attribute Selectors**

![image](img2/cap1.PNG)



