# Javascript
**how javascript makes web pages more interactive** 
+ ACCESS CONTENT
You can use JavaScript to select any
element, attribute, or text from an HTML pages.

+ MODIFY CONTENT
You can use JavaScript to add
elements, attributes, and text to the
page, or remove them. For example:
1.  Add a paragraph of text after the
first < hl > element2.
2.  Change the value of c 1 ass
attributes to trigger new CSS rules
for those elements
3. Change the size or position of an
< img > element.
+ PROGRAM RULES
You can specify a set of steps for
the browser to follow (like a recipe),
which allows it to access or change the
content of a page.
+ REACT TO EVENTS
You can specify that a script should run
when a specific event has occurred. For
example, it could be run when:
1. A button is pressed
2. A link is clicked (or tapped) on
3. A cursor hovers over an element
4. Information is added to a form
5. An interval of time has passed
6. A web page has finished loading

EXAMPLES OF JAVASCRIPT
IN THE BROWSER Being:

**Access** the content of the page

**Modify** the content of the page

**Program** rules or instructions the browser can follow

**React** to events triggered by the user or browser

Validating forms (checking whether they have been
filled in correctly) is important when information is
supplied by users. **JavaScript** **lets you alert** the user
if mistakes have been made. It can also perform
sophisticated calculations based on any data entered
and reveal the results to the user.

***JavaScript is used to change the contents of an HTML page.***

What is a Scrept ?
**A script** is a series of instructions that a
computer can follow to achieve a goal.
We can compare the script by
* RECIPES
* HANDBOOKS
* MANUALS

WRITING A SCRIPT:
To write a script, you need to first
state your goal and then list the
tasks that need to be completed in
order to achieve it.


**EXPRESSIONS**

An expression evaluates into (results in) a single value. Broadly speaking
there are two types of expressions:

1. EXPRESSIONS THAT JUST ASSIGN A
VALUE TO A VARIABLE

In order for a variable to be useful, it needs to be
given a value. As you have seen, this is done using
the assignment operator (the equals sign).
var color = 'beige';
The value of co 1 or is now beige.

2. EXPRESSIONS THAT USE TWO OR
MORE VALUES TO RETURN A
SINGLE VALUE

You can perform operations on any number of
individual values (see next page) to determine a
single value. For example:
var area = 3 * 2;
The value of area is now 6.


**OPERATORS:**  Expressions rely on things called operators; they allow programmers to
create a single value from one or more values.
* ASSIGNMENT OPERATORS
Assign a value to a variable
color = 'beige';
The value of co 1 or is now beige.
* ARITHMETIC OPERATORS
Perform basic math
area = 3 * 2;
The value of area is now 6.
* STRING OPERATORS
Combine two strings
greeting= 'Hi 1 + 'Mol ly';
The value of greeting is now Hi Molly.
* COMPARISON OPERATORS
Compare two values and return true or fa 1 se
buy = 3 > 5;
The value of buy is fa 1 se.

* LOGICAL OPERATORS
Combine expressions and return true or fa 1 se
buy= (5 > 3) && (2 < 4);
The value of buy is now true.

**A BASIC FUNCTION**
Before the closing < /body >
tag, you can see the link to the
JavaScript file. The JavaScript
file starts with a variable used
to hold a new message, and is
followed by a function ca lled
updateMessage().
like the example below in HTML:
< script src="js/ basic-function .js"></ script>

 IN JAVASCRIPT
var msg = 'Sign up to receive our newsletter for 10% off!';
function updateMessage() {
var el = document.getElementByld('message'};
el .textContent = msg;
}
updateMessage(};



