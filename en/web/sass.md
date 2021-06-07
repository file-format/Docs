---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass File Format
linktitle: Sass
description: Learn about Sass file format and APIs that can create and open Sass files.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## What is a SASS file? ##

Sass (syntactically awesome style sheets) is a preprocessor scripting language. It is compiled into [CSS](/web/css/) and is stored with the .sass extension. Sass consists of two syntaxes, the original based on indentations that uses the .sass extension and the newer SCSS with block formatting like CSS that uses the .scss extension.

## Why use Sass ##

Sass is really helpful in maintaining styles as it provides many features like introduces variables, nesting, mixins, imports, and selector inheritance that make working with styles fun.

## How to use SASS files ##

SASS files are not included directly in the [HTML](/web/html/) document but are rather converted to CSS files that are included in HTML files. You may istall Sass of your system by following the instructions given on the [Official Sass Site](https://sass-lang.com/install).

Sass may be converted to CSS by either converting an already saved SASS file or by watching for changes and converting as the file is saved. The commands for both are given below.

### Convert Once ###

The first parameter of the command is the source SASS file and the second parameter is the output CSS file.

```cmd
sass main.sass main.css
```

### Watch for Changes ###

The above command can be run with an additional *watch* flag that keeps the command running and as soon as the Sass file is saved, output CSS is generated.

```cmd
sass --watch main.sass main.css
```

## Sass Syntax ##

Sass supports variables, nesting, mixins, imports, selector inheritance, etc. Given below are examples of these features.

### Variables ###

Variables can be used to set reusable information such as primary color or padding for a button. This can prove useful if in the future you needed to change that information, you just change it at one location and it updates everywhere.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**Generated CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Nesting ###

CSS selectors can be nested similar to the hierarchy of HTML. In the following example, the span is nested inside the h1 block.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**Generated CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Mixins ###

Mixins are used to group similar properties together that are used in multiple places. Mixins also support parameters.

**Sass**

**Declaring a mixin**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Using a mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Generated CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Extend ###

Extend/Inheritance can prove to be useful in cases where the properties of one selector need to be shared with another selector. In the example below, the *.error-notice* selector takes all the properties of the *.error-text* selector and adds border and padding properties.

**Sass**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**Generated CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Import ###

Importing can be useful if you structure your styles into different files based on functionality or any other structure that you follow. You may import all these files in a primary SASS file that is later converted to CSS. While importing, you do not need to specify the file extension in the import instruction. Sass compiles all SASS files directly. To avoid import files to be compiled directly, you can make them partials by adding underscore(_) at the start of their name. Partials are imported similar to normal Sass files.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

The output CSS will have the styles from all the imported files.

## References ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)
