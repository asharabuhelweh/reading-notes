# Object Literals
**Objects** group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names.

If a variable is part of an object, it is called a
**property**. *Properties te ll us about the object*, such as
the name of a hotel or the number of rooms it has.
Each individual hotel might have a different name
and a different number of rooms.


**IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES**

**IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS**

Like variables and named functions,
properties and methods have a
**name and a value.** In an object,
that **name is called a key**.

![image](img2/cap2.PNG)


![image](img2/cap3.PNG)


**Accessing Object Properties**

 You can access object properties in two ways:

1. using dot `objectName.propertyName`
2. using  square bracket  `objectName["propertyName"]`


CREATING OBJECTS USING
LITERAL NOTATION

![image](img2/cap4.PNG)

**The this Keyword**

In a function definition, this refers to the "owner" of the function.

## Document Object Model
The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window.

With the object model, JavaScript gets all the power it needs to create dynamic HTML:
* JavaScript can change all the HTML elements in the page
* JavaScript can change all the HTML attributes in the page
* JavaScript can change all the CSS styles in the page
* JavaScript can remove existing HTML elements and attributes
* JavaScript can add new HTML elements and attributes
* JavaScript can react to all existing HTML events in the page
* JavaScript can create new HTML events in the page


The HTML DOM is a standard object model and programming interface for HTML. It defines:

* The HTML elements as objects
* The properties of all HTML elements
* The methods to access all HTML elements
* The events for all HTML elements

THE DOM TREE IS A MODEL OF A WEB PAGE
As a browser loads a web page, it creates a model of that page.
The model is called**a DOM tree**, and it is stored in the browsers' memory.
It consists of four main types of nodes.

![image](img2/cap5.PNG)

* ATTRIBUTE NODES

  The opening tags of HTML elements can carry
attributes and these are represented by attribute
nodes in the DOM tree.

* TEXT NODES
 Once you have accessed an element node, you
can then reach the text within that element. This is
stored in its own text node.

**WORKING WITH THE DOM TREE**

Accessing and updating the DOM tree involves two steps:

1. Locate the node that represents the element you want to work with.
2. Use its text content, child elements, and attributes.

STEP 1: ACCESS THE ELEMENTS

Here are three common ways to
select an individual element:

1. getElementByld ()
2. querySe1ector ()  Uses a CSS selector, and returns the first matching element.

3. You can also select individual
elements by **traversing from one element to another within the DOM tree**

**SELECT MULTIPLE ELEMENTS (NODELISTS)**

1. getElementsByClassName()
2. getElementsByTagName()
3. querySelectorAll() *Uses a CSS selector to select all matching elements.*


**TRAVERSING BETWEEN ELEMENT NODES**

You can move from one element
node to a related element node.
1. **parentNode** Selects the parent of the current
element node (which will return
just one element).
2. previousSibling / nextSibling
3. firstChild / lastChild


**STEP 2: WORK WITH THOSE ELEMENTS**
1. ACCESS/ UPDATE
TEXT NODES
2. WORK WITH HTML
CONTENT
3. ACCESS OR UPDATE
ATTRIBUTE VALUES


![image](img2/cap6.PNG)

LOOPING THROUGH
A NODELIST

![image](img2/cap7.PNG)









