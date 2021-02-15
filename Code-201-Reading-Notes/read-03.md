# HTML Lists, Control Flow with JS, and the CSS Box Model

## Lists
1. **Ordered lists** are lists where each item in the list is
numbered. For example, the list might be a set of steps for
a recipe that must be performed in order, or a legal contract
where each point needs to be identified by a section
number.

     the ordered list is created with the `<ol>` element.

2. **Unordered lists** are lists that begin with a bullet point
(rather than characters that indicate order).
 
     the unordered list is created with the `<ul>` element.
     
3. **Definition lists** are made up of a set of terms along with the definitions for each of those terms

   The definition list is created with the `<dl>` element and usually
consists of a series of terms and their definitions.

   * `<dt>` This is used to contain the term being defined (the definition term).

   * `<dd>`This is used to contain the definition.

  **Nested Lists**    `<li>`
  You can put a second list inside an `<li>` element to create a sublist or nested list.

## Boxes
Box Dimensions (width, height)
All HTML elements can be considered as boxes. In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model.

Limiting Width
min-width, max-width

**CSS Borders**

The CSS border properties allow you to specify the style, width, and color of an element's border.
The border-style property specifies what kind of border to display.

The following values are allowed:

* dotted - Defines a dotted border
* dashed - Defines a dashed border
* solid - Defines a solid border
* double - Defines a double borderborder-color value
* ridge - Defines a 3D ridged border. The effect depends on the border-color value
* inset - Defines a 3D inset border. The effect depends on the border-color value
* outset - Defines a 3D outset border. The effect depends on the border-color value
* none - Defines no border
hidden - Defines a hidden border


**CSS Border Width**
The border-width property specifies the width of the four borders.

The width can be set as a specific size (in px, pt, cm, em, etc) or by using one of the three pre-defined values: **thin, medium, or thick**

 **Border Color**
The border-color property is used to set the color of the four borders.

The color can be set by:

* name - specify a color name, like "red"
* HEX - specify a HEX value, like "#ff0000"
* RGB - specify a RGB value, like "rgb(255,0,0)"
* HSL - specify a HSL value, like "hsl(0, 100%, 50%)"
* transparent

 **Padding**


The CSS padding properties are used to generate space around an element's content, inside of any defined borders.


With CSS, you have full control over the padding. There are properties for setting the padding for each side of an element **(top, right, bottom, and left).**


  ### Tables
  Bullet Point Styles

  **The list-style-type** property allows you to control the shape
or style of a bullet point (also known as a marker).


For an unordered list you can use
the following values:
* none
* disc
* circle
* square

For an ordered (numbered) list
you can use the following values:
* decimal
1 2 3
* decimal-leading-zero
01 02 03
* lower-alpha
a b c
* upper-alpha
A B C
* lower-roman
i. ii. iii.
* upper-roman
I II III

### ARRAYS
An array is a special type of variable. It doesn't
just store one value; it stores a list of values.

Creating an Array
sing an array literal is the easiest way to create a JavaScript Array.

Syntax:

var array_name = [item1, item2, ...];


### LOOPS
Loops check a condition. If it returns **true**, a code block will **run**. Then the condition will be **checked again** and if it **still** **returns true**, the code block will **run again**. It **repeats** until the condițion returns **false.**

 ### There are three common types of loops:
 FOR 

WHILE

 DO WHILE 

- **FOR** 

  If you need to run code ***a specific number of times***, use a **for loop**. (It is the most common loop.) 

- **WHILE**

   If you **do not know how many times the code should run**, you can use a ***while loop***. Here the condition can be something other than a counter, and **the code will continue to loop for as long as the condition is true.**

* **WHILE DO**
The do...while loop is very similar to the while loop, but has one key difference: **it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.**

![PIC](images/Capture2.PNG)

### LOOPS COUNTERS
1. INITIALIZATION
 creat a variable and set it 0 

     var = 0

2. Condition 

the loop should continue to until the counter reach a specific number.

 for example: i>25

3. UPDATE 

 every time the loop has run it adds one to the counter.

  i++

