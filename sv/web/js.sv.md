---
date: 2019-10-11
keywords: js, .js, js filformat, hur man öppnar js-filer, javascript-filer
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS filformat
linktitle: JS
description: "Lär dig om JS-filformat och API:er som kan skapa och öppna JS-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Vad är JS fil? ##

JS (JavaScript) är filer som innehåller JavaScript-kod för exekvering på webbsidor. JavaScript-filer lagras med tillägget .js. I dokumentet [HTML](/sv/web/html/) kan du antingen bädda in JavaScript-koden med hjälp av \ <script>\</script> taggar eller inkludera en JS-fil. I likhet med [CSS](/sv/web/css/)-filer kan JS-filer inkluderas i flera HTML-dokument för återanvändning av kod. JavaScript kan användas för att manipulera HTML DOM.

## Kortfattad bakgrund ##

JavaScript skickades först som en del av Navigator Browser i september 1995 med namnet LiveScript av Netscape. Tre månader senare döptes det om till JavaScript. 1996 omvandlade Microsoft Navigators tolk för att skapa JScript. JScript släpptes med Internet Explorer och var väldigt annorlunda än JavaScript.

Netscape skickade in JavaScript till ECMA International som ledde till den officiella releasen av den första ECMAScript-specifikationen 1997. ECMAScript 2 släpptes 1998, ECMAScript 3 1999, och arbetet med ECMAScript 4 började 2000 men nådde aldrig resultat.

Jesse James Garrett släppte 2005 en vitbok där han myntade termen *Ajax*. Detta använde JavaScript som ryggrad för att skapa webbapplikationer som laddade data i bakgrunden och undvek att ladda om hela sidan. Detta resulterade i skapandet av bibliotek som JQuery, Prototype, Dojo, etc.

Google släppte webbläsaren Chrome med V8 JavaScript-motorn 2008. I början av 2009 slöts ett avtal om att kombinera allt relevant arbete och driva JavaScript framåt. Detta resulterade i lanseringen av ECMAScript 5 Standard i december 2009.

## Hur man använder JS-filer ##

För att använda en JS-fil inkluderar du den i HTML-dokumentet. Du använder länktaggen för att inkludera filen som visas nedan.

```html
<script src="site.js"></script>
```

*src*-attributet för *script*-taggen innehåller sökvägen till JS-filen. Genom att göra detta läggs JS-funktionaliteten till i HTML-dokumentet.

## JS-syntax ##

JavaScript-filer kan innehålla variabler, operatorer, funktioner, villkor, loopar, arrayer, objekt, etc. Nedan ges en kort översikt över JavaScript-syntaxen.

- Varje kommando slutar med ett semikolon(;).
- Använd nyckelordet *var* för att deklarera variabler.
- Stöder aritmetiska operatorer ( + - * / ) för att beräkna värden.
- Enradskommentarer läggs till med // och flerradskommentarer omges av /* och */.
- Alla identifierare är skiftlägeskänsliga, dvs *modelNo* och *modelno* är två olika variabler.
- Funktioner definieras genom att använda nyckelordet *function*.
- Arrayer kan definieras med hakparenteser [].
- JS stöder jämförelseoperatorer som ==, != , >=, !==, etc.
- Klasser kan definieras med nyckelordet *class*.

## JS-användningsexempel ##

Följande visar ett enkelt användningsexempel på JavaScript-fil.

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

### JS-kod ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referenser ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

