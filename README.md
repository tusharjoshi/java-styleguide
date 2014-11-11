# Java Style Guide

*Opinionated Java style guide for teams by [@tusharvjoshi](//twitter.com/tusharvjoshi)*

If you are looking for an opinionated style guide for syntax, conventions, and structuring Java code, then step right in. This way of writing style guide is heavily inspired from [@john_papa](//twitter.com/john_papa). 

## Table of Contents

  1. [Source File Structure](#source-file-structure)
  1. [IIFE](#iife)
  1. [References](#references)
  
## Source File Structure

### Order of elements

Order of the elements in a Java source file shall be

  1. License section
  1. package declaration
  1. import statements
  1. Functional comment for top level class
  1. Class declaration
  
### License section

  File shall start with a license statement.  For open source projects as well as commercial projects there is usually a license which comes here in a multiline comment.
  
### Package declaration

  The package statement is not line-wrapped. The column limit does not apply to package statements.
  
### Import statements

  - no wildcard imports in static or normal imports
  - no import statements (IDE provides feature of fixing import statement which shall be used before committing the source file)
  - Import statements are not line-wrapped. The column limit does not apply to import statements.
  
### Functional comment for top level class

  There shall be a functional Javadoc comment for the top level class mentioning the usage of the class.  Main dependencies and calling mechanism which is not obviious from the source.
  
### Class declaration
####Exactly one top level class

  Each top-level class resides in a source file of its own.
  
####  Class elements ordering

The ordering of the members of a class can have a great effect on learnability, but there is no single correct recipe for how to do it. Different classes may order their members differently.

What is important is that each class order its members in some logical order, which its maintainer could explain if asked. For example, new methods are not just habitually added to the end of the class, as that would yield "chronological by date added" ordering, which is not a logical ordering.  

**[Back to top](#table-of-contents)**

## IIFE
### JavaScript Closures

  - Wrap AngularJS components in an Immediately Invoked Function Expression (IIFE). 
  
  *Why?*: An IIFE removes variables from the global scope. This helps prevent variables and function declarations from living longer than expected in the global scope, which also helps avoid variable collisions.

  *Why?*: When your code is minified and bundled into a single file for deployment to a production server, you could have collisions of variables and many global variables. An IIFE protects you against both of these by providing variable scope for each file.
  
**[Back to top](#table-of-contents)**

## References

These references are the starting points of this style guide.  Many more additions and changes are done on these initial styles.  Newly revealed patterns like clean code by Robert C Martin have influenced many of the styles in this list.

  - [Google Java Style Guide] (//google-styleguide.googlecode.com/svn/trunk/javaguide.html)
  - [Java Programming Style Guide] (//alumnus.caltech.edu/~croft/research/java/guide/)
  - [Central Washington Uni - Java Programming Style Guide] (//www.cwu.edu/~gellenbe/javastyle/)
  - [Java Ranch - Java Programming Style Guide] (//www.javaranch.com/style.jsp)
  - [Cay Horstmann's - Java Programming Style Guide] (//www.horstmann.com/bigj2/style.html)