---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS-tiedostolomakeat
linktitle: JS
description: Lansaitse JS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JS-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Mikä on JS-tiedosto? ##

JS (JavaScript) ovat tiedostoja, jotka sisältävät JavaScript-koodin suorittamista varten verkkosivuilla. JavaScript-tiedostot tallennetaan .js-tunnisteella. [HTML](/web/html/)-dokumentin sisään voit joko upottaa JavaScript-koodin käyttämällä \ <script>\</script> -tunnisteita tai sisältää JS-tiedoston. Kuten [CSS](/web/css/)-tiedostot, JS-tiedostot voidaan sisällyttää useisiin HTML-dokumentteihin koodin uudelleenkäytettävyyttä varten. JavaScriptiä voidaan käyttää manipuloimaan HTML DOM:ia.

## Lyhyt historia ##

JavaScript toimitettiin ensimmäisen kerran osana Navigator-selainta syyskuussa 1995 Netscapen nimellä LiveScript. Kolme kuukautta myöhemmin se nimettiin uudelleen JavaScriptiksi. Vuonna 1996 Microsoft käänsi Navigatorin tulkin JScriptin luomiseksi. JScript julkaistiin Internet Explorerin kanssa ja oli hyvin erilainen kuin JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 julkaistiin vuonna 1998, ECMAScript 3 vuonna 1999, ja työ ECMAScript 4:n parissa aloitettiin vuonna 2000, mutta se ei koskaan saavuttanut tulosta.

Jesse James Garrett julkaisi vuonna 2005 valkoisen kirjan, jossa hän loi termin *Ajax*. Tämä käytti JavaScriptiä selkärankana verkkosovellusten luomiseen, jotka latasivat tietoja taustalla ja välttyivät koko sivun uudelleenlataamiselta. Tämä johti kirjastojen, kuten JQuery, Prototype, Dojo jne., luomiseen.

Google released the Chrome browser with the V8 JavaScript engine in 2008. Vuoden 2009 alussa tehtiin sopimus kaiken asiaankuuluvan työn yhdistämisestä ja JavaScriptin viemisestä eteenpäin. Tämä johti ECMAScript 5 -standardin julkaisuun joulukuussa 2009.

## Kuinka käyttää JS-tiedostoja ##

Jos haluat käyttää JS-tiedostoa, sisällytä se HTML-dokumenttiin. Käytät linkkitunnistetta sisällyttääksesi tiedoston alla olevan kuvan mukaisesti.

```html
<script src="site.js"></script>
```

*script*-tunnisteen *src*-attribuutti sisältää polun JS-tiedostoon. Näin JS-toiminto lisätään HTML-dokumenttiin.

## JS-syntaksi ##

JavaScript-tiedostot voivat sisältää muuttujia, operaattoreita, toimintoja, ehtoja, silmukoita, taulukoita, objekteja jne. Alla on lyhyt katsaus JavaScriptin syntaksiin.

- Jokainen komento päättyy puolipisteeseen (;).
- Käytä *var*-avainsanaa muuttujien ilmoittamiseen.
- Supports arithmetic operators ( + - * / ) arvojen laskemiseen.
- Yksiriviset kommentit lisätään //-merkillä ja monirivisiä kommentteja ympäröi /* ja */.
- Kaikki tunnisteet ovat kirjainkoolla eroteltuja eli *modelNo* ja *modelno* ovat kaksi eri muuttujaa.
- Funktiot määritellään avainsanalla *function*.
- Taulukot voidaan määrittää hakasulkeilla [].
- JS tukee vertailuoperaattoreita, kuten ==, != , >=, !== jne.
- Luokat voidaan määrittää käyttämällä *class*-avainsanaa.

## JS-käyttöesimerkki ##

Seuraavassa on yksinkertainen käyttöesimerkki JavaScript-tiedosto.

### HTML-dokumentti ###

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

### JS-koodi ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Viitteet ##

- {{HYPERLINKKI1}}

