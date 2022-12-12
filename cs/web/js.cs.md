---
date: 2019-10-11
keywords: js, .js, formát souborů js, jak otevřít soubory js, soubory javascript
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru JS
linktitle: JS
description: "Přečtěte si o formátu souborů JS a rozhraních API, která mohou vytvářet a otevírat soubory JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Co je soubor JS? ##

JS (JavaScript) jsou soubory, které obsahují kód JavaScript pro spuštění na webových stránkách. Soubory JavaScript jsou uloženy s příponou .js. Do dokumentu [HTML](/cs/web/html/) můžete buď vložit kód JavaScript pomocí \ <script>\</script> tagy nebo zahrnout soubor JS. Podobně jako u souborů [CSS](/cs/web/css/) mohou být soubory JS zahrnuty do více dokumentů HTML pro opětovné použití kódu. JavaScript lze použít k manipulaci s HTML DOM.

## Stručná historie ##

JavaScript byl poprvé dodán jako součást prohlížeče Navigator v září 1995 pod názvem LiveScript od Netscape. O tři měsíce později byl přejmenován na JavaScript. V roce 1996 Microsoft reverzně analyzoval interpret Navigator, aby vytvořil JScript. JScript byl vydán s Internet Explorerem a byl velmi odlišný od JavaScriptu.

Netscape zaslal JavaScript ECMA International, což vedlo k oficiálnímu vydání první specifikace ECMAScript v roce 1997. ECMAScript 2 byl vydán v roce 1998, ECMAScript 3 v roce 1999 a práce na ECMAScript 4 začaly v roce 2000, ale nikdy nedosáhly svého uskutečnění.

Jesse James Garrett v roce 2005 vydal bílou knihu, kde vytvořil termín *Ajax*. To využívalo JavaScript jako páteř k vytváření webových aplikací, které načítaly data na pozadí a vyhýbaly se opětovnému načítání celé stránky. To vedlo k vytvoření knihoven jako JQuery, Prototype, Dojo atd.

Google vydal prohlížeč Chrome s V8 JavaScript enginem v roce 2008. Počátkem roku 2009 byla uzavřena dohoda o spojení všech relevantních prací a posouvání JavaScriptu vpřed. To vedlo k vydání standardu ECMAScript 5 v prosinci 2009.

## Jak používat soubory JS ##

Chcete-li použít soubor JS, zahrňte jej do dokumentu HTML. Pomocí značky odkazu zahrnete soubor, jak je znázorněno níže.

```html
<script src="site.js"></script>
```

Atribut *src* značky *script* obsahuje cestu k souboru JS. Tím se do dokumentu HTML přidá funkce JS.

## JS syntaxe ##

Soubory JavaScriptu mohou obsahovat proměnné, operátory, funkce, podmínky, smyčky, pole, objekty atd. Níže je uveden stručný přehled syntaxe JavaScriptu.

- Každý příkaz končí středníkem(;).
- K deklaraci proměnných použijte klíčové slovo *var*.
- Podporuje aritmetické operátory ( + - * / ) pro výpočet hodnot.
- Jednořádkové komentáře jsou přidány pomocí // a víceřádkové komentáře jsou obklopeny /* a */.
- Všechny identifikátory rozlišují velká a malá písmena, tj. *modelNo* a *modelno* jsou dvě různé proměnné.
- Funkce jsou definovány pomocí klíčového slova *function*.
- Pole lze definovat pomocí hranatých závorek [].
- JS podporuje operátory porovnání jako ==, != , >=, !== atd.
- Třídy lze definovat pomocí klíčového slova *class*.

## Příklad použití JS ##

Následující text ukazuje jednoduchý příklad použití souboru JavaScript.

### HTML dokument ###

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

## Reference ##

- [JS - Wikipedie](https://en.wikipedia.org/wiki/JavaScript)

