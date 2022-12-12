---
date: 2019-10-11
keywords: css, .css, format de fișier css, cum se deschide fișiere css, foi de stil în cascadă
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier CSS
linktitle: CSS
description: "Aflați despre formatul de fișier CSS și despre API-urile care pot crea și deschide fișiere CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Ce este un fișier CSS? ##

CSS (Cascading Style Sheets) sunt fișiere care descriu modul în care elementele HTML sunt afișate pe ecran, hârtie etc. Cu HTML, puteți avea fie stiluri încorporate, fie stiluri pot fi definite într-o foaie de stil externă. Pentru încorporarea stilurilor, \ <style>\</style> sunt folosite etichete. Foile de stil externe sunt stocate în fișiere cu extensia .css. Cu CSS extern, îl puteți include pe mai multe pagini HTML pentru a actualiza stilul acestor pagini. Chiar și un singur fișier CSS poate fi folosit pentru a stila un site web complet.

## Scurt istoric ##

CSS1 a fost lansat în 1996, cu Bert Bos ca co-autor. Grupul de lucru CSS a început să lucreze la problemele care nu au fost abordate în CSS1. Acest lucru a dus la crearea CSS2 în noiembrie 1997, care a fost publicat ca recomandare W3C la 12 mai 1998. Această versiune a adăugat suport pentru dispozitive specifice media, cum ar fi imprimante, fonturi descărcabile, tabele și poziționarea elementelor. În iunie 1999, CSS3 a devenit recomandarea W3C. Aceasta a împărțit documentația în module în care fiecare modul avea caracteristici de extensie definite în CSS2.

## Cum se utilizează fișierele CSS ##

Pentru a utiliza un fișier CSS, îl includeți în secțiunea de cap a documentului HTML. Utilizați eticheta de link pentru a include fișierul, așa cum se arată mai jos.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

atributul *href* al etichetei link conține calea către fișierul CSS. Făcând acest lucru, stilurile aplicabile conținute în fișierul CSS inclus sunt aplicate documentului HTML.

## Sintaxa CSS ##

O regulă CSS constă din două componente, un selector și o declarație. Un selector indică un element din documentul HTML. Poate fi fie o etichetă de element, un nume de clasă, un nume de id, mai multe etichete care arată ierarhia, etc. O declarație conține definiția stilului care cuprinde proprietate și valoare. Proprietatea identifică proprietatea elementului pe care doriți să-l modificați, iar valoarea definește noua sa valoare. Fiecare regulă CSS poate avea mai multe declarații. Următorul este un exemplu de regulă CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

În exemplul de mai sus, avem **h1** ca selector care selectează toate etichetele h1 din documentul HTML. Regula are două declarații, una pentru greutatea fontului și cealaltă pentru culoare. *greutatea fontului* și *culoarea* sunt proprietăți, iar *700* și, respectiv, *forestgreen* sunt valorile lor.

## Exemplu de utilizare CSS ##

Următoarele arată exemplul de document HTML și foaia de stil folosită pentru stil. Imaginea de comparație este adăugată și pentru a compara documentele HTML simple și stilate

### Document HTML ###

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

### Foaie de stil CSS ###

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

### Comparație de ieșiri ###

Partea stângă a imaginii afișează documentul HTML fără stilurile aplicate, iar partea dreaptă afișează documentul HTML cu stilurile aplicate.

{{< figure src="../CssExample.jpg" alt="Imagine exemplu" >}}

## Referințe ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

