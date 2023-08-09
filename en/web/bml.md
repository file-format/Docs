{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BML File Format - Bean Markup Language File",
  "description":"Learn about BML file format and APIs that can create and open BML files.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-08-12"
}

## What is a BML file?

A file with .bml extension is a Bean Markup Language file that stores Java classes for supporting Java apps. This allows access to Java objects and methods, and doesn't need to create new functionality using Java classes. It specifies how the components are connected to each other for performing useful tasks. BML was developed by IBM alphaWorks to describe the structures and components relationships. BML files can be opened and viewed using any text editor such as Web Browsers, Microsoft Notepad and Notepad++.

## BML File Format

The IBM alphaworks website has provided two implementations of BML. The First implementation is an interpreter that 'plays' a BML script for generating the desired bean hierarchy. The second implementation is a compiler that compiles any BML script into reflection-free Java code. This is advantageous in the sense that it allows capturing the inter-component structure of the application using a language that is designed for this specific purpose with the added ability to compile it into 'regular' Java code.

## BML Tags

The following is an explanation of some of the tags used in the BML language:

### The <bean> tag:

The <bean> element is used to create new beans or to look up beans by name. The <bean> tag is of the format:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
The "id" in the tag is associated with the object registry for the JavaBean.

### The <string> tag

There are two ways the string tag can be used:

 1. To create a non-empty string:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. To create an empty string:

```
<string/>
```
## References

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)

