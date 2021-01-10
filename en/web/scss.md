---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS File Format
linktitle: SCSS
description: Learn about SCSS file format and APIs that can create and open SCSS files.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## What is an SCSS file? ##

SCSS is the second syntax of Sass (Syntactically Awesome Stylesheet) that uses brackets instead of indentations. SCSS was designed in such a way that a valid CSS3 file is also a valid SCSS file. SCSS files are stored with the .scss extension.

## Why use SCSS ##

As the designs of websites are becoming complex resulting in large [CSS](/web/css/) files. Such files are harder to maintain. This is where SCSS comes in. SCSS introduces variables, nesting, mixins, imports, and selector inheritance in CSS development. These additions make working with design a lot more fun.

## How to open SCSS files ##

SCSS files are stored in plain text format so these can be opened in any text editor including the following:

- Notepad
- Notepad ++
- VS Code
- Visual Studio
- PhpStorm
- Adobe Dreamweaver

## How to use SCSS files ##

SCSS files are not included directly in the [HTML](/web/html/) document like CSS. Instead, SCSS files are converted to CSS files that are included in HTML files. To install SCSS on your system, follow the instructions given on the [Official Sass Site](https://sass-lang.com/install).
To convert SCSS to CSS, you may either convert an already saved SCSS file or watch for changes and convert as the file is saved. The commands for both are given below.

### Convert Once ###

The first parameter is the source SCSS file and the second parameter is the output CSS file.

```cmd
sass main.scss main.css
```

### Watch for Changes ###

The command has an additional *watch** flag that keeps the command running and as soon as the SCSS file is saved, output CSS is generated.

```cmd
sass --watch main.scss main.css
```

## SCSS Syntax ##

SCSS supports variables, nesting, mixins, imports, selector inheritance, etc. Given below are examples of these features.

### Variables ###

By the use of variables, you can set reusable information such as primary color or background color for the save button. This is useful if you need to change that information, you just change it at one location and it updates where ever it is used.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

You can nest the CSS selectors similar to the hierarchy of HTML. In the example given below, the span is nested inside the h1 block.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Mixins can be used to group similar properties together that are used together in multiple places. You can also pass parameters to mixins.

**SCSS**

**Declaring a mixin**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Using a mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Extend/Inheritance is useful in cases where the properties of one selector need to be shared with another selector. In the example below, the *.error-notice* selector takes all the properties of *.error-text* selector and adds border and padding properties.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

Importing can be useful in the separation of concerns. You may divide the styles in such a way that the header styles are in a separate file, the footer styles are in a separate file, all the color variables used in the styles can be in a separate file, etc. Using this technique, the styles stay organized. You just import the files in your main SCSS file as shown in the example below. You do not need to specify the file extension in the import instruction. Sass compiles all SCSS files directly. To avoid import files to be compiled directly, you can make them partials by adding underscore(_) before their name. You can import partials similar to normal SCSS files without the underscore.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

The output CSS will have the styles from all the imported files.

## References ##

- [SCSS Introduction - W3schools](https://www.w3schools.com/sass/default.php)
- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)
