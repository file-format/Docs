---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS fil formularat
linktitle: CSS
description: Ltjene om CSS filformat og API'er, der kan oprette og åbne CSS fils.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Hvad er en CSS fil? ##

CSS (Cascading Style Sheets) er filer, der beskriver, hvordan HTML-elementer vises på skærmen, papir osv. Med HTML kan du enten have indlejrede styles eller stile kan defineres i et eksternt stylesheet. Til indlejring af typografierne skal \ <style>\</style> tags bruges. De eksterne stylesheets gemmes i filer med .css-udvidelsen. Med den eksterne CSS kan du inkludere den på flere HTML-sider for at opdatere stilen på disse sider. Selv en enkelt CSS-fil kan bruges til at style et komplet websted.

## Kort historie ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Dette resulterede i oprettelsen af CSS2 i november 1997, der blev offentliggjort som en W3C-anbefaling den 12. maj 1998. Denne version tilføjede understøttelse af mediespecifikke enheder som printere, skrifttyper, der kan downloades, tabeller og elementpositionering. I juni 1999 blev CSS3 W3C's anbefaling. Dette opdelte dokumentationen i moduler, hvor hvert modul havde udvidelsesfunktioner defineret i CSS2.

## Sådan bruger du CSS-filer ##

For at bruge en CSS-fil skal du inkludere den i hovedafsnittet i HTML-dokumentet. Du bruger link-tagget til at inkludere filen som vist nedenfor.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

*href*-attributten for link-tagget indeholder stien til CSS-filen. Ved at gøre dette, anvendes de relevante stilarter, der er indeholdt i den inkluderede CSS-fil, på HTML-dokumentet.

## CSS-syntaks ##

En CSS-regel består af to komponenter, en vælger og en erklæring. En vælger peger på et element i HTML-dokumentet. Det kan enten være et element-tag, klassenavn, id-navn, flere tags, der viser hierarkiet osv. En erklæring indeholder stildefinitionen bestående af egenskab og værdi. Egenskaben identificerer egenskaben for det element, du vil ændre, og værdien definerer dens nye værdi. Hver CSS-regel kan have flere erklæringer. Det følgende er et eksempel på en CSS-regel.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

I ovenstående eksempel har vi **h1** som en vælger, der vælger alle h1-tags i HTML-dokumentet. Reglen har to erklæringer, en for skrifttypevægt og den anden for farve. *font-weight* og *color* er egenskaber og *700* og *forestgreen* er deres værdier.

## Eksempel på CSS-brug ##

Det følgende viser HTML-eksemplet og det typografiark, der bruges til at style det. Sammenligningsbilledet tilføjes også for at sammenligne de stylede og almindelige HTML-dokumenter

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

### Output sammenligning ###

Den venstre side af billedet viser HTML-dokumentet uden de anvendte typografier, og den højre side viser HTML-dokumentet med de anvendte typografier.

{{< figure src="../CssExample.jpg" alt="Eksempelbillede" >}}

## Referencer ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

