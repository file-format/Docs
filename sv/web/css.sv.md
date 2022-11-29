---
date: 2019-10-11
keywords: css, .css, css-filformat, hur man öppnar css-filer, överlappande stilmallar
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS filformat
linktitle: CSS
description: "Lär dig mer om CSS-filformat och API:er som kan skapa och öppna CSS-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Vad är en CSS-fil? ##

CSS (Cascading Style Sheets) är filer som beskriver hur HTML-element visas på skärmen, papper etc. Med HTML kan du antingen ha inbäddade stilar eller så kan stilar definieras i en extern stilmall. För att bädda in stilarna, <style>\</style> taggar används. De externa stilmallarna lagras i filer med filtillägget .css. Med den externa CSS kan du inkludera den på flera HTML-sidor för att uppdatera stilen på dessa sidor. Även en enda CSS-fil kan användas för att utforma en komplett webbplats.

## Kortfattad bakgrund ##

CSS1 släpptes 1996 med Bert Bos som medförfattare. CSS-arbetsgruppen började arbeta med de frågor som inte togs upp i CSS1. Detta resulterade i skapandet av CSS2 i november 1997 som publicerades som en W3C-rekommendation den 12 maj 1998. Denna version lade till stöd för mediaspecifika enheter som skrivare, nedladdningsbara typsnitt, tabeller och elementpositionering. I juni 1999 blev CSS3 W3C:s rekommendation. Detta delade upp dokumentationen i moduler där varje modul hade tilläggsfunktioner definierade i CSS2.

## Hur man använder CSS-filer ##

För att använda en CSS-fil, inkluderar du den i huvuddelen av HTML-dokumentet. Du använder länktaggen för att inkludera filen som visas nedan.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

*href*-attributet för länktaggen innehåller sökvägen till CSS-filen. Genom att göra detta tillämpas de tillämpliga stilarna i den medföljande CSS-filen på HTML-dokumentet.

## CSS-syntax ##

En CSS-regel består av två komponenter, en väljare och en deklaration. En väljare pekar på ett element i HTML-dokumentet. Det kan antingen vara en elementtagg, klassnamn, id-namn, flera taggar som visar hierarkin, etc. En deklaration innehåller stildefinitionen som består av egenskap och värde. Egenskapen identifierar egenskapen för det element som du vill ändra och värdet definierar dess nya värde. Varje CSS-regel kan ha flera deklarationer. Följande är ett exempel på en CSS-regel.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

I exemplet ovan har vi **h1** som en väljare som väljer alla h1-taggar i HTML-dokumentet. Regeln har två deklarationer, en för teckensnittsvikt och den andra för färg. *font-weight* och *color* är egenskaper och *700* respektive *skogsgrön* är deras värden.

## CSS-användningsexempel ##

Följande visar exempel på HTML-dokumentet och formatmallen som används för att utforma det. Jämförelsebilden läggs också till för att jämföra formaterade och vanliga HTML-dokument

### HTML-dokument ###

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

### CSS-formatmall ###

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

### Utgångsjämförelse ###

Den vänstra sidan av bilden visar HTML-dokumentet utan de tillämpade stilarna och den högra sidan visar HTML-dokumentet med stilarna tillämpade.

{{< figure src="../CssExample.jpg" alt="Exempelbild" >}}

## Referenser ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

