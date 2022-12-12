---
date: 2019-10-11
keywords: js, .js, js fájlformátum, js fájlok megnyitása, javascript fájlok
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS fájlformátum
linktitle: JS
description: "Ismerje meg a JS fájlformátumot és az API-kat, amelyek JS-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Mi az a JS fájl? ##

A JS (JavaScript) olyan fájlok, amelyek JavaScript kódot tartalmaznak a weboldalakon való végrehajtáshoz. A JavaScript-fájlok tárolása .js kiterjesztéssel történik. A [HTML](/hu/web/html/) dokumentumba beágyazhatja a JavaScript kódot a \ <script>\</script> címkéket, vagy tartalmazzon JS-fájlt. A [CSS](/hu/web/css/) fájlokhoz hasonlóan a JS-fájlok több HTML-dokumentumban is szerepelhetnek a kód újrafelhasználhatósága érdekében. A JavaScript használható a HTML DOM manipulálására.

## Rövid története ##

A JavaScriptet először a Navigator Browser részeként szállította 1995 szeptemberében LiveScript néven a Netscape. Három hónappal később átnevezték JavaScriptre. 1996-ban a Microsoft a Navigator értelmezőjét fordította a JScript létrehozására. A JScript az Internet Explorerrel jelent meg, és nagyon különbözött a JavaScripttől.

A Netscape benyújtotta a JavaScriptet az ECMA International-nek, ami az első ECMAScript specifikáció hivatalos kiadásához vezetett 1997-ben. Az ECMAScript 2 1998-ban, az ECMAScript 3 1999-ben jelent meg, és az ECMAScript 4-en való munka 2000-ben kezdődött, de soha nem értek el.

Jesse James Garrett 2005-ben kiadott egy fehér könyvet, amelyben megalkotta az *Ajax* kifejezést. Ez a JavaScriptet használta gerincként olyan webalkalmazások létrehozásához, amelyek a háttérben töltötték be az adatokat, és elkerülték a teljes oldal újratöltését. Ennek eredményeként olyan könyvtárak jöttek létre, mint a JQuery, Prototype, Dojo stb.

A Google 2008-ban kiadta a Chrome böngészőt V8 JavaScript motorral. 2009 elején megállapodás született az összes lényeges munka egyesítéséről és a JavaScript előremozdításáról. Ennek eredményeként 2009 decemberében megjelent az ECMAScript 5 Standard.

## JS fájlok használata ##

JS-fájl használatához fel kell vennie azt a HTML-dokumentumba. A fájl beillesztéséhez használja a link címkét az alábbiak szerint.

```html
<script src="site.js"></script>
```

A *script* címke *src* attribútuma tartalmazza a JS-fájl elérési útját. Ezzel a JS funkció hozzáadódik a HTML dokumentumhoz.

## JS szintaxis ##

A JavaScript fájlok tartalmazhatnak változókat, operátorokat, függvényeket, feltételeket, ciklusokat, tömböket, objektumokat stb. Az alábbiakban rövid áttekintést adunk a JavaScript szintaxisáról.

- Minden parancs pontosvesszővel(;) végződik.
- Használja a *var* kulcsszót a változók deklarálásához.
- Támogatja az aritmetikai operátorokat ( + - * / ) az értékek kiszámításához.
- Az egysoros megjegyzéseket a // karakterrel egészíti ki, a többsoros megjegyzéseket pedig /* és */ veszi körül.
- Minden azonosító megkülönbözteti a kis- és nagybetűket, azaz a *modelNo* és a *modelno* két különböző változó.
- A függvények meghatározása a *function* kulcsszó használatával történik.
- A tömbök szögletes zárójelekkel [] definiálhatók.
- A JS támogatja az olyan összehasonlító operátorokat, mint az ==, != , >=, !== stb.
- Az osztályok a *class* kulcsszó használatával határozhatók meg.

## JS használati példa ##

Az alábbiakban egy egyszerű használati példa JavaScript-fájlt mutatunk be.

### HTML dokumentum ###

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

### JS kód ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Hivatkozások ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

