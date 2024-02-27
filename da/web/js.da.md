---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS-filformularat
linktitle: JS
description: Ltjene om JS filformat og API'er, der kan oprette og åbne JS fils.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Hvad er JS fil? ##

JS (JavaScript) er filer, der indeholder JavaScript-kode til kørsel på websider. JavaScript-filer gemmes med filtypenavnet .js. Inde i [HTML](/web/html/)-dokumentet kan du enten indlejre JavaScript-koden ved hjælp af \ <script>\</script> tags eller inkludere en JS-fil. I lighed med [CSS](/web/css/)-filer kan JS-filer inkluderes i flere HTML-dokumenter for genbrug af kode. JavaScript kan bruges til at manipulere HTML DOM.

## Kort historie ##

JavaScript blev først sendt som en del af Navigator Browser i september 1995 med navnet LiveScript af Netscape. Det blev omdøbt til JavaScript tre måneder senere. I 1996 omvendte Microsoft Navigators tolk til at skabe JScript. JScript blev udgivet med Internet Explorer og var meget anderledes end JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 blev udgivet i 1998, ECMAScript 3 i 1999, og arbejdet med ECMAScript 4 begyndte i 2000, men nåede aldrig ud i livet.

Jesse James Garrett udgav i 2005 en hvidbog, hvor han opfandt udtrykket *Ajax*. Dette brugte JavaScript som en rygrad til at skabe webapplikationer, der indlæste data i baggrunden og undgik genindlæsning af hele sider. Dette resulterede i oprettelsen af biblioteker som JQuery, Prototype, Dojo osv.

Google released the Chrome browser with the V8 JavaScript engine in 2008. I begyndelsen af 2009 blev der indgået en aftale om at kombinere alt relevant arbejde og drive JavaScript fremad. Dette resulterede i udgivelsen af ECMAScript 5-standarden i december 2009.

## Sådan bruger du JS-filer ##

For at bruge en JS-fil skal du inkludere den i HTML-dokumentet. Du bruger link-tagget til at inkludere filen som vist nedenfor.

```html
<script src="site.js"></script>
```

*src*-attributten for *script*-tagget indeholder stien til JS-filen. Ved at gøre dette føjes JS-funktionaliteten til HTML-dokumentet.

## JS-syntaks ##

JavaScript-filer kan indeholde variabler, operatorer, funktioner, betingelser, loops, arrays, objekter osv. Nedenfor er givet en kort oversigt over JavaScripts syntaks.

- Hver kommando slutter med et semikolon(;).
- Brug nøgleordet *var* til at erklære variabler.
- Supports arithmetic operators ( + - * / ) for at beregne værdier.
- Enkeltlinjekommentarer tilføjes med // og flerlinjekommentarer er omgivet af /* og */.
- Alle identifikatorer skelner mellem store og små bogstaver, dvs. *modelNo* og *modelno* er to forskellige variable.
- Funktioner defineres ved at bruge nøgleordet *funktion*.
- Arrays kan defineres ved hjælp af firkantede parenteser [].
- JS understøtter sammenligningsoperatorer som ==, != , >=, !== osv.
- Klasser kan defineres ved hjælp af *class* nøgleordet.

## JS-brugseksempel ##

Det følgende viser et simpelt eksempel på en JavaScript-fil.

### HTML-dokument ###

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

### JS-kode ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referencer ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

