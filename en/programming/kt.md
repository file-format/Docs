---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file format, kt extension, .kt extention
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT File Format
linktitle: KT
description: Learn about KT file format and APIs that can create and open KT files.
menu:
  docs:
    parent: "programming"
lastmod: 2020-17-12
---

## What is a KT file? ##

Kotlin is a general-purpose cross-platform programming language developed by JetBrains to be fully interoperable with [Java](/programming/java/). The Kotlin source code is contained in a file with the .kt extension. The Kotlin trademark is protected by the Kotlin Foundation.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 started supporting Kotlin as an alternative for Android App development in October 2017.

## Brief History ##

Kotlin was unveiled by JetBrains in July 2011 as a new programming language for JVM. The lead of JetBrains Dmitry Jemerov said that most of the languages were missing features that they were looking for except Scala but the slow compilation of Scala was a drawback. One of the main goals of Kotlin was to compile as quickly as Java. The Kotlin project was open-sourced under Apache 2 License in February 2012.

Version 1.0 of Kotlin was released on 15 February 2015. Android announced first-class support for Kotlin on Android at Google I/O 2017. Kotlin 1.2 was released on 28 November 2017 with the ability to share code between JVM and JavaScript platforms. Kotlin 1.3 was released on 29 October 2018 with the support for asynchronous programming. Google announced Kotlin to be the preferred programming language for Android App development on 7 May 2019. Kotlin 1.4 was released in August 2020 with some slight changes to support interoperability with Swift/Objective-C.

## Kotlin Syntax ##

Kotlin was designed to be better than Java but still be interoperable with Java code to allow gradual migration from Java to Kotlin.

Semicolons are optional in Kotlin. A new line is enough to indicate the end of the statement.

Kotlin supports two types of variables, read-only, defined by the *val* keyword, and mutable, defined by the *var* keyword.

Classes are private and final by default. To derive from a class, the base class has to be declared with the *open* keyword.

Kotlin also supports procedural programming.

The entry point to the Kotlin program is the "main" function similar to Java, C#, etc.

### Syntax Example ###

The following is an example of Kotlin syntax.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

In the above code, the **fun** keyword defines the function named main. Inside the function, a read-only variable 'audience' is declared with the **val** keyword. By using the **println** method, "Hello World from Kotlin" is printed on the console. The value of the variable audience is injected into the string with the **$** sign.

## How to open KT files ##

Kotlin files can be opened by using the following programs.

- IntelliJ Idea
- Google Android Studio
- NetBeans
- Eclipse

## References ##

- [Kotlin (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))
