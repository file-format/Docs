---
date: 2019-10-11
keywords: js, .js, format de fișier js, cum se deschide fișiere js, fișiere javascript
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier JS
linktitle: JS
description: "Aflați despre formatul de fișier JS și despre API-urile care pot crea și deschide fișiere JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Ce este un fișier JS? ##

JS (JavaScript) sunt fișiere care conțin cod JavaScript pentru execuție pe paginile web. Fișierele JavaScript sunt stocate cu extensia .js. În documentul [HTML](/ro/web/html/), puteți fie să încorporați codul JavaScript folosind \ <script>\</script> etichete sau includ un fișier JS. Similar cu fișierele [CSS](/ro/web/css/), fișierele JS pot fi incluse în mai multe documente HTML pentru reutilizarea codului. JavaScript poate fi folosit pentru a manipula HTML DOM.

## Scurt istoric ##

JavaScript a fost livrat pentru prima dată ca parte a Navigator Browser în septembrie 1995 cu numele LiveScript de Netscape. A fost redenumit JavaScript trei luni mai târziu. În 1996, Microsoft a realizat o inginerie inversă a interpretului Navigator pentru a crea JScript. JScript a fost lansat cu Internet Explorer și era foarte diferit de JavaScript.

Netscape a trimis JavaScript la ECMA International, ceea ce a dus la lansarea oficială a primei specificații ECMAScript în 1997. ECMAScript 2 a fost lansat în 1998, ECMAScript 3 în 1999, iar lucrul la ECMAScript 4 a început în 2000, dar nu a ajuns niciodată la bun sfârșit.

Jesse James Garrett a lansat în 2005 o carte albă în care a inventat termenul *Ajax*. Aceasta a folosit JavaScript ca coloană vertebrală pentru a crea aplicații web care au încărcat date în fundal și au evitat reîncărcările întregii pagini. Acest lucru a dus la crearea de biblioteci precum JQuery, Prototype, Dojo etc.

Google a lansat browserul Chrome cu motorul JavaScript V8 în 2008. La începutul lui 2009, a fost încheiat un acord pentru a combina toate lucrările relevante și pentru a promova JavaScript. Acest lucru a dus la lansarea standardului ECMAScript 5 în decembrie 2009.

## Cum se utilizează fișierele JS ##

Pentru a utiliza un fișier JS, îl includeți în documentul HTML. Utilizați eticheta de link pentru a include fișierul, așa cum se arată mai jos.

```html
<script src="site.js"></script>
```

Atributul *src* al etichetei *script* conține calea către fișierul JS. Făcând acest lucru, funcționalitatea JS este adăugată documentului HTML.

## Sintaxa JS ##

Fișierele JavaScript pot conține variabile, operatori, funcții, condiții, bucle, matrice, obiecte etc. Mai jos este o scurtă prezentare generală a sintaxei JavaScript.

- Fiecare comandă se termină cu punct și virgulă (;).
- Utilizați cuvântul cheie *var* pentru a declara variabile.
- Suportă operatori aritmetici ( + - * / ) pentru a calcula valori.
- Comentariile pe o singură linie sunt adăugate cu // iar comentariile pe mai multe linii sunt înconjurate de /* și */.
- Toți identificatorii sunt sensibile la majuscule, adică *modelNo* și *modelno* sunt două variabile diferite.
- Funcțiile sunt definite folosind cuvântul cheie *funcție*.
- Matricele pot fi definite folosind paranteze drepte [].
- JS acceptă operatori de comparație precum ==, != , >=, !== etc.
- Clasele pot fi definite folosind cuvântul cheie *class*.

## Exemplu de utilizare JS ##

Următoarele arată un exemplu de fișier JavaScript simplu de utilizare.

### Document HTML ###

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

### Cod JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referințe ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

