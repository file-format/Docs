---
date: 2020-25-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: What are CSS files?
linktitle: CSS
description: CSS (Cascading Style Sheets) are files that describe how HTML elements are displayed on screen, paper, etc.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## What are CSS files? ##

CSS (Cascading Style Sheets) are files that describe how HTML elements are displayed on the screen, paper, etc. With HTML, you can have either embedded styles or styles can be defined in an external stylesheet. For embedding the styles, the \<style>\</style> tags are used. The external stylesheets are stored in files with the .css extension. With the external CSS, you can include it on multiple HTML pages to update the style of those pages. Even a single CSS file can be used to style a complete website.

## Brief History ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. This resulted in the creation of CSS2 in November 1997 that was published as a W3C recommendation on 12th May 1998. This version added support for media-specific devices like printers, downloadable fonts, tables, and element positioning. In June 1999, CSS3 became the recommendation of W3C. This divided the documentation into modules where each module had extension features defined in CSS2.

## How to open CSS files ##

CSS files are stored in plain text format so these can be opened in any text editor including the following:

- Notepad
- Notepad ++
- VS Code
- Visual Studio
- PhpStorm
- Adobe Dreamweaver

## How to use CSS files ##

To use a CSS file, you include it in the head section of the HTML document. You use the link tag to include the file as shown below.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

the *href* attribute of the link tag contains the path to the CSS file. By doing this, the applicable styles contained in the included CSS file are applied to the HTML document.

## CSS Syntax ##

A CSS rule comprises of two components, a selector and a declaration. A selector points to an element in the HTML document. It can either be an element tag, class name, id name, multiple tags showing the hierarchy, etc. A declaration contains the style definition comprising of property and value. The property identifies the property of the element that you want to change and the value defines its new value. Each CSS rule can have multiple declarations. The following is an example of a CSS rule.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

In the above example, we have the **h1** as a selector that selects all the h1 tags in the HTML document. The rule has two declarations, one for font-weight and the other for color. *font-weight* and *color* are properties and *700* and *forestgreen* are their values respectively.

## CSS Usage Example ##

The following shows the example HTML document and the stylesheet used to style it. The comparison image is also added to compare the styled and plain HTML documents

### HTML Document ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS Stylesheet ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Output Comparison ###

The left side of the image displays the HTML document without the styles applied and the right side displays the HTML document with the styles applied.

{{< figure src="../CssExample.jpg" alt="Example image" >}}

## References ##

- [CSS Introduction - W3schools](https://www.w3schools.com/css/default.asp)
- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)
