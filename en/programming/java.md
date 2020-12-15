---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java File Format
linktitle: Java
description: Java is a general-purpose object oriented language that can run on multiple platforms. The Java source code is contained in files with the .java extension.
menu:
  docs:
    parent: "programming"
lastmod: 2020-07-12
---

## What is a Java file? ##

Java is a general-purpose object-oriented language that can run on multiple platforms. The Java source code is contained in a file with the .java extension. Java is used for the development of mobile applications, web applications, desktop applications, games, etc. Java works on multiple platforms including Windows, Mac, Linux, Raspberry Pi, etc. Java is very similar to C# and C++ so it is easier to switch between these languages.

## Brief History ##

The Java project was initiated in June 1991 by James Gosling, Mike Sheridan, and Patrick Naughton. Java was initially named Oak. It was later renamed Green and finally to Java. James Gosling designed Java with a syntax similar to C/C++. The first public version of Java was released in 1996 by Sun Microsystems. It could run on all the popular systems which caused Java to become popular quickly. With the release of Java 2 in December 1998, multiple configurations for different types of platforms were built. The versions were as follows

- J2EE (Java EE): For enterprise solutions
- J2ME (Java ME): For mobile applications
- J2SE (Java SE): For desktop applications

On November 19, 2006, Java Virtual Machine (JVM) was released by Sun as free and open-source software. After Oracle Corporation acquired Sun Microsystems in 2009–2010, James Gosling resigned from Oracle on April 2, 2010.

## How to open Java files ##

You can use any text editor to view the text in Java files. Some of the options are given below.

- Notepad (this will not execute the script)
- VS Code
- Visual Studio
- IntelliJ Idea

## How to run/execute Java files ##

To execute the Java code, it needs to be compiled first. For that, the Java SDK is required. The Java SDK compiles the Java code to a bytecode class file. There are IDE's like Eclipse and IntelliJ Idea that makes it easier to work with Java files by providing code completion and easy to use interface to compile and execute the Java code.

## Java File Format ##

The syntax of Java was highly influenced by C and C++ but unlike C++, Java was built almost exclusively as an object-oriented language. In Java, all the code is written inside classes and every data item is an object. In contrast to C++, Java does not support operator overloading or multiple inheritance.

### Syntax ###

The following is an example of Java syntax.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
In the above code, the **public** keyword denotes the access modifier. It states that this class may be accessed by the classes outside the class hierarchy. The access modifier can also be **protected** (can be accessed in the same package) or **private** (the methods can only be accessed by the same class). The **static** in front of the method indicates that the method can be invoked without a specific instance of the class. The **void** indicates that the method would return nothing. To print the string to the console. System.out.println command is used. In this command, the *System* class has a static field *out* which is an instance of the *PrintStream* class containing the *println* method.

The file name of the Java files should be the same as the class name. So the Java file for the example code would be named *ExampleApp.java*.

## References ##

- [Java Introduction - W3schools](https://www.w3schools.com/java/default.asp)
- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))
