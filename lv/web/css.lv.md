---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS faila veidlapaat
linktitle: CSS
description: Lnopelniet par CSS faila formātu un API, kas var izveidot un atvērt CSS failus.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Kas ir CSS fails? ##

CSS (Cascading Style Sheets) ir faili, kas apraksta, kā HTML elementi tiek parādīti ekrānā, papīrā utt. Izmantojot HTML, varat iestatīt iegultos stilus vai stilus var definēt ārējā stilu lapā. Lai iegultu stilus, \ <style>\</style> tiek izmantoti tagi. Ārējās stilu lapas tiek glabātas failos ar paplašinājumu .css. Izmantojot ārējo CSS, varat to iekļaut vairākās HTML lapās, lai atjauninātu šo lapu stilu. Pat vienu CSS failu var izmantot, lai izveidotu visu vietni.

## Īsa vēsture ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Tā rezultātā 1997. gada novembrī tika izveidots CSS2, kas tika publicēts kā W3C ieteikums 1998. gada 12. maijā. Šī versija pievienoja atbalstu tādām multivides ierīcēm kā printeri, lejupielādējami fonti, tabulas un elementu pozicionēšana. 1999. gada jūnijā CSS3 kļuva par W3C ieteikumu. Tas sadalīja dokumentāciju moduļos, kur katram modulim bija paplašinājuma funkcijas, kas definētas CSS2.

## Kā lietot CSS failus ##

Lai izmantotu CSS failu, tas ir jāiekļauj HTML dokumenta galvenajā sadaļā. Lai iekļautu failu, izmantojiet saites tagu, kā parādīts tālāk.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

saites taga atribūts *href* satur ceļu uz CSS failu. To darot, HTML dokumentam tiek piemēroti piemērotie stili, kas ietverti iekļautajā CSS failā.

## CSS sintakse ##

CSS noteikums sastāv no diviem komponentiem, atlasītāja un deklarācijas. Atlasītājs norāda uz elementu HTML dokumentā. Tas var būt elementa tags, klases nosaukums, ID nosaukums, vairāki tagi, kas parāda hierarhiju utt. Deklarācijā ir ietverta stila definīcija, kas sastāv no īpašuma un vērtības. Rekvizīts identificē tā elementa rekvizītu, kuru vēlaties mainīt, un vērtība nosaka tā jauno vērtību. Katrai CSS kārtulai var būt vairākas deklarācijas. Tālāk ir sniegts CSS kārtulas piemērs.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Iepriekš minētajā piemērā mums ir **h1** kā atlasītājs, kas atlasa visus h1 tagus HTML dokumentā. Noteikumam ir divas deklarācijas: viena fonta svaram un otra krāsai. *font-weight* un *color* ir rekvizīti, un *700* un *forestgreen* ir attiecīgi to vērtības.

## CSS lietošanas piemērs ##

Tālāk ir parādīts HTML dokumenta piemērs un stila lapa, kas izmantota tā stila veidošanai. Salīdzinājuma attēls tiek pievienots arī, lai salīdzinātu veidotos un vienkāršus HTML dokumentus

### HTML dokuments ###

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

### CSS stila lapa ###

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

### Izejas salīdzinājums ###

Attēla kreisajā pusē tiek parādīts HTML dokuments bez lietotajiem stiliem, bet labajā pusē tiek parādīts HTML dokuments ar lietotajiem stiliem.

{{< figure src="../CssExample.jpg" alt="Attēla piemērs" >}}

## Atsauces Nr.

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

