# Text
**Headings** 

HTML has six "levels" of headings:
< h1> is used for main headings
< h2> is used for subheadings.

**Paragraph** < p>

To create a paragraph, surround the words that make up the
paragraph with an opening < p> tag and closing </ p> tag.

**Bold < b> & Italic < i>**

**Superscript**
The **< sub>** element is used to contain characters that should
be subscript. It is commonly used with foot notes or chemical
formulas such as H20.

**Line Breaks & Horizontal Rules**  
 add a line break inside the middle of a paragraph you can use the line break tag < br />.

To create a break between themes — such as a change oftopic in a book or a new scene
in a play — you can add a horizontal rule between sections using the **< hr />** tag.

**Semantic Markup**
There are some text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages — they are known as semantic markup.

**Strong & Emphasis**
The use of the < strong> element indicates that its content has strong importance.

The < em> element indicates emphasis that subtly changes
the meaning of a sentence. By default browsers will show the contents of an < em> element in *italic*

**Quotations** by tow ways:
1. The **< blockquote>** element is used for longer quotes that take
up an entire paragraph. Note how the < p> element is still
used inside the < blockquote> element.
2. The **< q>** element is used for shorter quotes that sit within
a paragraph.


## Introducing CSS
CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: **a selector and a declaration**.


![img](/image/img5.PNG)

* CSS Properties Affect How Elements Are Displayed


Using External CSS:
* < link> element can be used in an HTML document to tell the
browser where to find the CSS file used to style the page.
* < href>
This specifies the path to the CSS file.
* < type> This attribute specifies the type
of document being linked to. The value should be text/css.

* < rel> This specifies the relationship
between the HTML page and the file it is linked to.

**Using Internal CSS**
* < style>
 we used inside the < head> element of the page.

 **CSS Selectors**

![img](/image/img6.PNG)
![img](/image/img6.PNG)


## Basic JavaScript Instructions
A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a **statement**. 
* Statements should end with a semicolon.
* Each of the lines of code in green is a statement.
* The pink curly braces indicate the start and end
of a code block. (Each code block could contain
many more statements.)
* The code in purple determines which code
should run.

**COMMENTS**
* You should write comments to explain what your code does.
* They help make your code easier to read and understand.
* This can help you and others who read your code.

**variables** 

JavaScript variables are containers for storing data values.

**Declaring:** 

(Creating) JavaScript Variables
Creating a variable in JavaScript is called "declaring" a variable.

**data types:**
1. numbers
2. strings
3. BOOLEAN

EXAMPLE OF USING A VARIABLE TO STORE A NUMBER AND STRINGS: 

var x;           // Now x is undefined

x = 5;           // Now x is a Number

x = "REEM";      // Now x is a String


*CHANGING THE VALUE OF A VARIABLE:
Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.*



**JavaScript Arrays** 
An array is a special type of variable. It doesn't just store one value; it stores a list of values.
* JavaScript arrays are written with square brackets.

* Array items are separated by commas.
![img](/image/img7.PNG)





**EXPRESSIONS**
An expression evaluates into (results in) a single value.

there are two types of expressions.
1. EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE

EXP: var color = 'PINK';

2. EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE

EXP:  var size = 3 * 2 *6;

**OPERATORS**

* The assignment operator (=) assigns a value to a variable.

![img](/image/img8.PNG)


## Decisions and Loops

 **COMPARISON OPERATORS**
EVALUATING CONDITIONS You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: true or false.

* == is equal to

* != is not equal to
* === strict equal to
* !== strict not equal to
-   (>) greater than
*  < less than 
*  (>=) greater than or equal to
*  <= less than or equal to

## Logical Operators
 Logical and &&

 Logical or ||

 Logical not !

![pic](images/Capture.PNG)

![PIC](images/Capture.PNG)

