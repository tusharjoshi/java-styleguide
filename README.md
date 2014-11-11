# Java Style Guide

*Opinionated Java style guide for teams by [@tusharvjoshi](//twitter.com/tusharvjoshi)*

If you are looking for an opinionated style guide for syntax, conventions, and structuring Java code, then step right in. This way of writing style guide is heavily inspired from [@john_papa](//twitter.com/john_papa). 

## Table of Contents

  1. [Single Responsibility](#single-responsibility)
  1. [IIFE](#iife)
  1. [References](#references)
  
## Single Responsibility

### Rule of 1

  Contents here

**[Back to top](#table-of-contents)**

## IIFE
### JavaScript Closures

  - Wrap AngularJS components in an Immediately Invoked Function Expression (IIFE). 
  
  *Why?*: An IIFE removes variables from the global scope. This helps prevent variables and function declarations from living longer than expected in the global scope, which also helps avoid variable collisions.

  *Why?*: When your code is minified and bundled into a single file for deployment to a production server, you could have collisions of variables and many global variables. An IIFE protects you against both of these by providing variable scope for each file.
  
**[Back to top](#table-of-contents)**

## References

  - [Google Java Style Guide] (//google-styleguide.googlecode.com/svn/trunk/javaguide.html)
  - [Java Programming Style Guide] (//alumnus.caltech.edu/~croft/research/java/guide/)
  - [Central Washington Uni - Java Programming Style Guide] (//www.cwu.edu/~gellenbe/javastyle/)
  - [Java Ranch - Java Programming Style Guide] (//www.javaranch.com/style.jsp)
  - [Cay Horstmann's - Java Programming Style Guide] (//www.horstmann.com/bigj2/style.html)