---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS failo formaat
linktitle: CSS
description: Luždirbti apie CSS failo formatą ir API, kurios gali sukurti ir atidaryti CSS failąs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Kas yra CSS failas? ##

CSS (Cascading Style Sheets) yra failai, apibūdinantys, kaip HTML elementai rodomi ekrane, popieriuje ir t. t. Naudodami HTML galite turėti įterptus stilius arba stilius galima apibrėžti išoriniame stilių lape. Norėdami įdėti stilių, \ <style>\</style> naudojamos žymos. Išoriniai stilių lapai saugomi failuose su plėtiniu .css. Naudodami išorinį CSS galite įtraukti jį į kelis HTML puslapius, kad atnaujintumėte tų puslapių stilių. Net vienas CSS failas gali būti naudojamas visai svetainei sukurti.

## Trumpa istorija ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Dėl to 1997 m. lapkričio mėn. buvo sukurtas CSS2, kuris buvo paskelbtas kaip W3C rekomendacija 1998 m. gegužės 12 d. Ši versija papildė specialių laikmenų įrenginių, tokių kaip spausdintuvai, atsisiunčiami šriftai, lentelės ir elementų padėties nustatymas, palaikymą. 1999 m. birželį CSS3 tapo W3C rekomendacija. Tai suskirstė dokumentaciją į modulius, kuriuose kiekvienas modulis turėjo CSS2 apibrėžtas išplėtimo funkcijas.

## Kaip naudoti CSS failus ##

Norėdami naudoti CSS failą, įtraukite jį į HTML dokumento antraštės skyrių. Norėdami įtraukti failą, naudojate nuorodos žymą, kaip parodyta toliau.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

nuorodos žymos atribute *href* yra kelias į CSS failą. Tai darant, taikomi stiliai, esantys įtrauktame CSS faile, taikomi HTML dokumentui.

## CSS sintaksė Nr.

CSS taisyklė susideda iš dviejų komponentų: parinkiklio ir deklaracijos. Parinkiklis nurodo elementą HTML dokumente. Tai gali būti elemento žyma, klasės pavadinimas, ID pavadinimas, kelios žymės, rodančios hierarchiją ir tt Deklaracija apima stiliaus apibrėžimą, kurį sudaro ypatybė ir vertė. Ypatybė identifikuoja elemento, kurį norite pakeisti, ypatybę, o vertė apibrėžia naują jo vertę. Kiekviena CSS taisyklė gali turėti kelias deklaracijas. Toliau pateikiamas CSS taisyklės pavyzdys.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Aukščiau pateiktame pavyzdyje turime **h1** kaip parinkiklį, kuris pasirenka visas h1 žymas HTML dokumente. Taisyklėje yra dvi deklaracijos: viena skirta šrifto svoriui ir kita spalvai. *font-weight* ir *color* yra savybės, o *700* ir *forestgreen* yra atitinkamai jų reikšmės.

## CSS naudojimo pavyzdys Nr.

Toliau pateikiamas HTML dokumento pavyzdys ir stiliaus lapas, naudojamas jo stiliui sukurti. Palyginimo vaizdas taip pat pridedamas norint palyginti stilizuotus ir paprastus HTML dokumentus

### HTML dokumentas ###

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

### CSS stiliaus lapas ###

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

### Išvesties palyginimas ###

Kairėje vaizdo pusėje rodomas HTML dokumentas be pritaikytų stilių, o dešinėje – HTML dokumentas su pritaikytais stiliais.

{{< figure src="../CssExample.jpg" alt="Vaizdo pavyzdys" >}}

## Nuorodos Nr.

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

