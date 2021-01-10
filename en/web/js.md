---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS File Format
linktitle: JS
description: Learn about JS file format and APIs that can create and open JS files.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## What is a JS file? ##

JS (JavaScript) are files that contain JavaScript code for execution on web pages. JavaScript files are stored with the .js extension. Inside the [HTML](/web/html/) document, you can either embed the JavaScript code using the \<script>\</script> tags or include a JS file. Similar to [CSS](/web/css/) files, JS files can be included in multiple HTML documents for code reusability. JavaScript can be used to manipulate the HTML DOM.

## Brief History ##

JavaScript was first shipped as part of the Navigator Browser in September 1995 with the name LiveScript by Netscape. It was renamed JavaScript three months later. In 1996, Microsoft reverse-engineered Navigator's interpreter to create JScript. JScript was released with Internet Explorer and was very different than JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 was released in 1998, ECMAScript 3 in 1999, and work on ECMAScript 4 began in 2000 but never reached fruition.

Jesse James Garrett in 2005 released a white paper where he coined the term *Ajax*. This used JavaScript as a backbone to create web applications that loaded data in the background and avoided full page reloads. This resulted in the creation of libraries like JQuery, Prototype, Dojo, etc.

Google released the Chrome browser with the V8 JavaScript engine in 2008. In early 2009, an agreement was made to combine all relevant work and to drive JavaScript forward. This resulted in the release of the ECMAScript 5 Standard in December 2009.

## How to open JS files ##

JS files are stored in plain text format so these can be opened in any text editor including the following:

- Notepad
- Notepad ++
- VS Code
- Visual Studio
- PhpStorm
- Adobe Dreamweaver

## How to use JS files ##

To use a JS file, you include it in the HTML document. You use the link tag to include the file as shown below.

```html
<script src="site.js"></script>
```

The *src* attribute of the *script* tag contains the path to the JS file. By doing this, the JS functionality is added to the HTML document.

## JS Syntax ##

JavaScript files can contain variables, operators, functions, conditions, loops, arrays, objects, etc. Given below is a brief overview of the syntax of JavaScript.

- Each command ends with a semicolon(;).
- Use the *var* keyword to declare variables.
- Supports arithmetic operators ( + - * / ) to compute values.
- Single line comments are added with // and multiline comments are surrounded by /* and */.
- All identifiers are case-sensitive i.e. *modelNo* and *modelno* are two different variables.
- Functions are defined by using the *function* keyword.
- Arrays can be defined using square brackets [].
- JS supports comparison operators like ==, != , >=, !==, etc.
- Classes can be defined using the *class* keyword.

## JS Usage Example ##

The following shows a simple usage example JavaScript file.

### HTML Document ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS Code ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## References ##

- [JS Introduction - W3schools](https://www.w3schools.com/js/default.asp)
- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)
