---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS failo formaat
linktitle: JS
description: Luždirbti apie JS failo formatą ir API, kurios gali sukurti ir atidaryti JS failąs.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Kas yra JS failas? ##

JS (JavaScript) yra failai, kuriuose yra JavaScript kodas, skirtas vykdyti tinklalapiuose. JavaScript failai saugomi su plėtiniu .js. Dokumente [HTML](/web/html/) galite įterpti JavaScript kodą naudodami \ <script>\</script> žymas arba įtraukti JS failą. Panašiai kaip ir [CSS](/web/css/) failai, JS failai gali būti įtraukti į kelis HTML dokumentus, kad būtų galima pakartotinai naudoti kodą. JavaScript gali būti naudojamas manipuliuoti HTML DOM.

## Trumpa istorija ##

JavaScript pirmą kartą buvo pristatyta kaip Navigator naršyklės dalis 1995 m. rugsėjį Netscape pavadinimu LiveScript. Po trijų mėnesių jis buvo pervadintas į JavaScript. 1996 m. Microsoft sukūrė Navigator interpretatorių, kad sukurtų JScript. JScript buvo išleistas su Internet Explorer ir labai skyrėsi nuo JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 buvo išleistas 1998 m., ECMAScript 3 1999 m., o darbas su ECMAScript 4 prasidėjo 2000 m., bet taip ir nepasiekė rezultatų.

2005 m. Jesse'as Jamesas Garrettas išleido baltąjį dokumentą, kuriame sukūrė terminą *Ajax*. Tai naudojo JavaScript kaip pagrindą kuriant žiniatinklio programas, kurios įkeldavo duomenis fone ir išvengdavo viso puslapio įkėlimo iš naujo. Dėl to buvo sukurtos bibliotekos, tokios kaip JQuery, Prototype, Dojo ir kt.

Google released the Chrome browser with the V8 JavaScript engine in 2008. 2009 m. pradžioje buvo sudarytas susitarimas sujungti visus susijusius darbus ir skatinti JavaScript. Dėl to 2009 m. gruodžio mėn. buvo išleistas ECMAScript 5 standartas.

## Kaip naudoti JS failus ##

Norėdami naudoti JS failą, įtraukite jį į HTML dokumentą. Norėdami įtraukti failą, naudojate nuorodos žymą, kaip parodyta toliau.

```html
<script src="site.js"></script>
```

*script* žymos atribute *src* yra kelias į JS failą. Taip JS funkcija įtraukiama į HTML dokumentą.

## JS sintaksė ##

JavaScript failuose gali būti kintamųjų, operatorių, funkcijų, sąlygų, kilpų, masyvų, objektų ir kt. Toliau pateikiama trumpa JavaScript sintaksės apžvalga.

- Kiekviena komanda baigiasi kabliataškiu (;).
- Norėdami deklaruoti kintamuosius, naudokite raktinį žodį *var*.
- Supports arithmetic operators ( + - * / ) vertėms apskaičiuoti.
- Vienos eilutės komentarai pridedami su //, o kelių eilučių komentarai yra apsupti /* ir */.
– Visuose identifikatoriuose skiriamos didžiosios ir mažosios raidės, ty *modelNo* ir *modelno* yra du skirtingi kintamieji.
- Funkcijos apibrėžiamos naudojant raktinį žodį *function*.
- Masyvai gali būti apibrėžti naudojant laužtinius skliaustus [].
- JS palaiko palyginimo operatorius, tokius kaip ==, != , >=, !== ir kt.
- Klasės gali būti apibrėžtos naudojant raktinį žodį *klasė*.

## JS naudojimo pavyzdys Nr.

Toliau pateikiamas paprastas JavaScript failo naudojimo pavyzdys.

### HTML dokumentas ###

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

### JS kodas ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Nuorodos Nr.

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

