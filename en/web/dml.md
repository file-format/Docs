{
  "date" : "2021-05-25",
  "keywords" : [ "DML","DML file", "DML file format", "DML file type", "file", "type", "what is a DML file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DML - DynaScript HTML File",
  "description":"Learn about DML file format and APIs that can create and open DML files.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-25"
}

## What is a DML file?

A file with .dml extension is a web script page code file created with DyanScript. DynaScript is a dynamic [HTML](/web/html/) scripting language that is compatible with ECMAScript and provides most of the same features as other scripting language. It is similar to ColdFusion code and Microsoft Active Server Pages (ASP) code. DML files can be opened and viewed in standard web browsers similar to other HTML pages.

## DML File Format

DML files are created in plain text file format and can be opened with a text editor to view the code. Code writing using DML scripting language can be used to dynamically generate HTML on server side hosted DML pages. DynaScripts are built from the following language elements:


 * SCRIPT tag - These are embedded in documents as HTML comments. An HTML comment is marked by a \<!-- tag.
 * Literals - These are fixed values in  DynaScript files. Examples of these include integers sucha s 123 , 0x3F , 0123, floating-point numbers such as 456.789 , 3.2e-8, Boolean such as true or false, and string such as "The rain in Spain"
 * Variables - DynaScript variables need not be defined or assign them to a fixed datatype. A variable must have a value before you use it in an expression; otherwise a runtime warning is generated.
 * Expressions - These are combinations of variables, literal values, operators, and other expressions. The right side of an assignment statement is an expression.
 * Operators - These operate on one or more expressions called operands. These can be either ternary, binary or unary: ternary operators act on three expressions, binary operators act on two expressions, and unary operators act on one.
 * Statements - These control script flow, manipulate objects, and general programming. In general, these statements follow standard C and Java syntax. Examples are if-else, do-while loops, switch, break, continue, etc. like any other scripting language.
* Functions - Functions, like any other scripting language, allow you to encapsulate a set of instructions once in a document as a function, then use it several times throughout the document (by calling the function). DynaScript also supports functions.
* Objects - DynaScript is object-oriented and supports `objects` and the fundamental object-oriented concepts of Encapsulation, Polymorphism, and Inheritance.

## References

* [DML](http://www.upi.pr.it/docs/dynref/pdreferencep8.htm)
