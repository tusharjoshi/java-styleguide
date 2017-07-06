# Java Style Guide

*Opinionated Java Style Guide for Teams by [@tusharvjoshi](//twitter.com/tusharvjoshi)*

If you are looking for an opinionated style guide for syntax, conventions, and structuring Java code, then step right in. This way of writing style guide is heavily inspired from [@john_papa](//twitter.com/john_papa). 

## Table of Contents

  1. [Source File Structure](#source-file-structure)
     1. [File Name](#file-name)
     1. [File encoding](#file-encoding)
     1. [Order of elements](#order-of-elements)
  1. [Packages](#packages)
  1. [Constants](#constants)
  1. [Variables](#variables)
  1. [Classes](#classes)
  1. [Functions](#functions)
  1. [Comments](#comments)
  1. [References](#references)
  
## Source File Structure

### File Name

The source file name consists of the case-sensitive name of the top-level class it contains (of which there is exactly one), plus the .java extension.

? Why: As dectated by Java compiler rules.

? Why: Only one top level class is recommended and that class name 
should be the file name

### File encoding

Source files are encoded in UTF-8.

? Why: This will support cross platform and cross locale source

? How: Modern IDEs have support for the encoding as global or project
settings

? Same as: Google Style Guide section 2.2

### Order of elements

Order of the elements in a Java source file shall be

  1. License section
  1. package declaration
  1. import statements
  1. Functional comment for top level class
  1. Class declaration
  1. Constants
  
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

**[Back to top](#table-of-contents)**

## Packages

### Package Identification

Packages shall be named starting with the reverse company name
for example com.company.project.module

? Why: To avoid namespace collision.

### Package capitalization and words

Package names shall be all small letters and single words 
separated by dots.

For example:
```java
package com.company.product.module;
```

**[Back to top](#table-of-contents)**

## Constants
### Constants specific to functionality

Constants shall be kept in the class nearer to the functionality.  They should not be kept in a common constant class.

? Why: Keeping constants in one common constants class is not maintainable.  When there is a change in any of the constants it introduces potential regression for all the areas where this Constants class is used.

? Other references: [Stackoverflow discussion](//stackoverflow.com/questions/66066/what-is-the-best-way-to-implement-constants-in-java/66076#66076)

```java
/* avoid */
public class Constants {
	public static final String RATEOFINTEREST_TYPE = "Simple";
	public static final String WELCOME_MESSAGE = "Welcome";
}
```

```java
/* recommended */
public class InterestCalculator {
	public static final String RATEOFINTEREST_TYPE = "Simple";
	
	/* other code */
}

public class WelcomeView {
	public static final String WELCOME_MESSAGE = "Welcome";
}
```

**[Back to top](#table-of-contents)**

## Variables

**[Back to top](#table-of-contents)**
  
## Classes

### Exactly one top level class

  Each top-level class resides in a source file of its own.
  
###  Class elements ordering

The ordering of the members of a class can have a great effect on learnability, but there is no single correct recipe for how to do it. Different classes may order their members differently.

What is important is that each class order its members in some logical order, which its maintainer could explain if asked. For example, new methods are not just habitually added to the end of the class, as that would yield "chronological by date added" ordering, which is not a logical ordering. 

**[Back to top](#table-of-contents)** 

## Functions

**[Back to top](#table-of-contents)**

## Comments

**[Back to top](#table-of-contents)**

## References

These references are the starting points of this style guide.  Many more additions and changes are done on these initial styles.  Newly revealed patterns like clean code by Robert C Martin have influenced many of the styles in this list.

  - [OpenJDK Community Guide](http://cr.openjdk.java.net/~alundblad/styleguide/index-v6.html)
  - [Google Guide] (https://google.github.io/styleguide/javaguide.html)
  - [Java Programming Style Guide] (http://alumnus.caltech.edu/~croft/research/java/guide/)
  - [Java Ranch Guide] (http://www.javaranch.com/style.jsp)
  - [Cay Horstmann's Guide] (http://www.horstmann.com/bigj2/style.html)
  - [GeoSoft Guide] (http://geosoft.no/development/javastyle.html)
  - [SEI CERT Oracle Coding Standard for Java] (https://www.securecoding.cert.org/confluence/display/java/SEI+CERT+Oracle+Coding+Standard+for+Java)
  
**[Back to top](#table-of-contents)**  
