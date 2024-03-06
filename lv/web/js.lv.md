---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS faila veidlapaat
linktitle: JS
description: Lnopelniet par JS faila formātu un API, kas var izveidot un atvērt JS failus.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Kas ir JS fails? ##

JS (JavaScript) ir faili, kas satur JavaScript kodu izpildei tīmekļa lapās. JavaScript faili tiek glabāti ar paplašinājumu .js. Dokumentā [HTML](/web/html/) varat iegult JavaScript kodu, izmantojot \ <script>\</script> tagus vai iekļaut JS failu. Līdzīgi kā [CSS](/web/css/) failos, JS failus var iekļaut vairākos HTML dokumentos, lai nodrošinātu koda atkārtotu izmantošanu. JavaScript var izmantot, lai manipulētu ar HTML DOM.

## Īsa vēsture ##

JavaScript pirmo reizi tika piegādāts kā daļa no pārlūkprogrammas Navigator 1995. gada septembrī ar nosaukumu LiveScript no Netscape. Trīs mēnešus vēlāk tas tika pārdēvēts par JavaScript. 1996. gadā Microsoft apgrieztā inženierijā izstrādāja Navigator tulku, lai izveidotu JScript. JScript tika izlaists kopā ar Internet Explorer un ļoti atšķiras no JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 tika izlaists 1998. gadā, ECMAScript 3 1999. gadā, un darbs pie ECMAScript 4 tika sākts 2000. gadā, taču tas nekad nesasniedza rezultātus.

Džesijs Džeimss Garets 2005. gadā izdeva balto grāmatu, kurā viņš ieviesa terminu *Ajax*. Tas izmantoja JavaScript kā mugurkaulu, lai izveidotu tīmekļa lietojumprogrammas, kas ielādēja datus fonā un izvairījās no pilnas lapas atkārtotas ielādes. Tā rezultātā tika izveidotas tādas bibliotēkas kā JQuery, Prototype, Dojo utt.

Google released the Chrome browser with the V8 JavaScript engine in 2008. 2009. gada sākumā tika noslēgta vienošanās apvienot visu attiecīgo darbu un virzīt JavaScript uz priekšu. Tā rezultātā 2009. gada decembrī tika izlaists ECMAScript 5 standarts.

## Kā lietot JS failus ##

Lai izmantotu JS failu, tas ir jāiekļauj HTML dokumentā. Lai iekļautu failu, izmantojiet saites tagu, kā parādīts tālāk.

```html
<script src="site.js"></script>
```

Taga *script* atribūts *src* satur ceļu uz JS failu. To darot, JS funkcionalitāte tiek pievienota HTML dokumentam.

## JS sintakse ##

JavaScript faili var saturēt mainīgos, operatorus, funkcijas, nosacījumus, cilpas, masīvus, objektus utt. Tālāk ir sniegts īss JavaScript sintakses pārskats.

- Katra komanda beidzas ar semikolu (;).
- Izmantojiet atslēgvārdu *var*, lai deklarētu mainīgos.
- Supports arithmetic operators ( + - * / ), lai aprēķinātu vērtības.
- Vienas rindiņas komentāri tiek pievienoti ar // un vairāku rindiņu komentārus ieskauj /* un */.
- Visi identifikatori ir reģistrjutīgi, ti, *modelNo* un *modelno* ir divi dažādi mainīgie.
- Funkcijas tiek definētas, izmantojot atslēgvārdu *funkcija*.
- Masīvus var definēt, izmantojot kvadrātiekavas [].
- JS atbalsta salīdzināšanas operatorus, piemēram, ==, != , >=, !== utt.
- Klases var definēt, izmantojot atslēgvārdu *klase*.

## JS lietošanas piemērs ##

Tālāk ir parādīts vienkāršs JavaScript faila lietojuma piemērs.

### HTML dokuments ###

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

### JS kods ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Atsauces Nr.

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

