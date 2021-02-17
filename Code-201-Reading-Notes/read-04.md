# HTML Links, CSS Layout, JS Functions
## LINKS
Links are the defining feature of the web
because they allow you to move from
one web page to another — enabling the
very idea of browsing or surfing.

HTML Links - Syntax

The HTML `<a>` tag defines a hyperlink. It has the following syntax:

`<a href="url">link text</a>`

Linking to Other Sites
`<a href="site link">text</a>`

Linking to Other Pages
on the Same Site we
can use a shorthand known as a
relative URL.

**Directory Structure**

![img](image/img9.PNG)

**Relative URLs**
Relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.

![](image/img10.PNG)

**Email Links**
`<a href="mailto:jon@example.org">Email Jon</a>`

**Opening Links in a New Window**
 using target

 `<a href="http://www.imdb.com" target="_blank">`


You can use the **id** attribute to target elements within
a page that can be linked to.

## Layout

Key Concepts in
Positioning Elements

Building Blocks
CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an **inline box**.

Block-level elements
start on a new line
Examples include:
`<h1> <p> <ul> <li>`

Inline elements
flow in between
surrounding text
Examples include:
`<img> <b> <i>`

### Functions, Methods, and Objects

Programmers use
functions, methods, and objects to organize their code.
This chapter is divided into three sections that introduce:
* FUNCTIONS 
* OBJECTS BUILT-IN
* METHODS OBJECTS

Functions let you group a series of statements together to perform a
specific task. If different parts of a script repeat the same task, you can
reuse the function (rather than repeating the same set of statements).

JavaScript Function Syntax
A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

**Function parameters** are listed inside the parentheses () in the function definition.

**Function arguments** are the values received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.


**Function Invocation**
The code inside the function will execute when "something" invokes (calls) the function:

When an event occurs (when a user clicks a button)
When it is invoked (called) from JavaScript code
Automatically (self invoked)

