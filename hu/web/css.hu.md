---
date: 2019-10-11
keywords: css, .css, css fájlformátum, css fájlok megnyitása, lépcsőzetes stíluslapok
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS fájl formátum
linktitle: CSS
description: "Ismerje meg a CSS fájlformátumot és az API-kat, amelyek CSS-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Mi az a CSS fájl? ##

A CSS (Cascading Style Sheets) olyan fájlok, amelyek leírják, hogy a HTML-elemek hogyan jelennek meg a képernyőn, papíron stb. A HTML-ben beágyazott stílusok is megadhatók, vagy stílusok definiálhatók egy külső stíluslapon. A stílusok beágyazásához a \ <style>\</style> címkéket használnak. A külső stíluslapok .css kiterjesztésű fájlokban tárolódnak. A külső CSS segítségével több HTML-oldalra is felveheti az oldalak stílusának frissítéséhez. Még egyetlen CSS-fájl is használható egy teljes webhely stílusához.

## Rövid története ##

A CSS1 1996-ban jelent meg Bert Bos társszerzővel. A CSS Munkacsoport azokon a kérdéseken kezdett dolgozni, amelyekkel a CSS1 nem foglalkozott. Ennek eredményeként 1997 novemberében létrejött a CSS2, amelyet W3C ajánlásként tettek közzé 1998. május 12-én. Ez a verzió támogatta a médiaspecifikus eszközöket, például nyomtatókat, letölthető betűtípusokat, táblázatokat és elempozícionálást. 1999 júniusában a CSS3 a W3C ajánlása lett. Ez modulokra osztotta a dokumentációt, ahol minden modul rendelkezik a CSS2-ben meghatározott kiterjesztési funkciókkal.

## A CSS-fájlok használata ##

CSS-fájl használatához fel kell vennie azt a HTML-dokumentum fejrészébe. A fájl beillesztéséhez használja a link címkét az alábbiak szerint.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

a link tag *href* attribútuma tartalmazza a CSS-fájl elérési útját. Ezzel a mellékelt CSS-fájlban található stílusok alkalmazásra kerülnek a HTML-dokumentumra.

## CSS szintaxis ##

A CSS-szabály két összetevőből áll, egy választóból és egy deklarációból. A választó egy elemre mutat a HTML-dokumentumban. Ez lehet egy elemcímke, osztálynév, azonosítónév, több címke, amely a hierarchiát mutatja stb. A deklaráció tartalmazza a tulajdonságot és az értéket tartalmazó stílusdefiníciót. A tulajdonság azonosítja a módosítani kívánt elem tulajdonságát, és az érték határozza meg az új értékét. Minden CSS-szabálynak több deklarációja lehet. A következő példa egy CSS-szabályra.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

A fenti példában a **h1** szelektort használjuk, amely kijelöli a HTML-dokumentum összes h1 címkéjét. A szabálynak két deklarációja van, az egyik a betűméretre, a másik a színre vonatkozik. A *font-weight* és a *color* a tulajdonságok, a *700* és a *forestgreen* pedig ezek értékei.

## CSS használati példa ##

Az alábbiakban bemutatjuk a HTML-dokumentum mintáját és a stíluslaphoz használt stíluslapot. Az összehasonlító kép a stílusos és az egyszerű HTML dokumentumok összehasonlításához is hozzáadásra kerül

### HTML dokumentum ###

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

### CSS-stíluslap ###

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

### Kimenetek összehasonlítása ###

A kép bal oldalán a HTML-dokumentum az alkalmazott stílusok nélkül, a jobb oldalon pedig a HTML-dokumentum az alkalmazott stílusokkal.

{{< figure src="../CssExample.jpg" alt="Példakép" >}}

## Hivatkozások ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

