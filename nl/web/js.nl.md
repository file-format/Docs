---
date: 2019-10-11
keywords: js, .js, js bestandsformaat, hoe js-bestanden te openen, javascript-bestanden
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS-bestandsindeling
linktitle: JS
description: "Meer informatie over JS-bestandsindelingen en API's die JS-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Wat is een JS-bestand? ##

JS (JavaScript) zijn bestanden die JavaScript-code bevatten voor uitvoering op webpagina's. JavaScript-bestanden worden opgeslagen met de extensie .js. In het [HTML](/nl/web/html/)-document kunt u de JavaScript-code insluiten met de \ <script>\</script> tags of voeg een JS-bestand toe. Net als bij [CSS](/nl/web/css/)-bestanden, kunnen JS-bestanden worden opgenomen in meerdere HTML-documenten voor herbruikbaarheid van code. JavaScript kan worden gebruikt om de HTML DOM te manipuleren.

## Korte geschiedenis ##

JavaScript werd voor het eerst geleverd als onderdeel van de Navigator Browser in september 1995 met de naam LiveScript door Netscape. Drie maanden later werd het omgedoopt tot JavaScript. In 1996 heeft Microsoft de tolk van Navigator reverse-engineered om JScript te maken. JScript werd uitgebracht met Internet Explorer en was heel anders dan JavaScript.

Netscape diende JavaScript in bij ECMA International, wat leidde tot de officiële release van de eerste ECMAScript-specificatie in 1997. ECMAScript 2 werd uitgebracht in 1998, ECMAScript 3 in 1999, en het werk aan ECMAScript 4 begon in 2000, maar kwam nooit tot bloei.

Jesse James Garrett bracht in 2005 een witboek uit waarin hij de term *Ajax* bedacht. Dit gebruikte JavaScript als ruggengraat om webapplicaties te maken die gegevens op de achtergrond laadden en het herladen van volledige pagina's vermeed. Dit resulteerde in de oprichting van bibliotheken zoals JQuery, Prototype, Dojo, enz.

Google lanceerde in 2008 de Chrome-browser met de V8 JavaScript-engine. Begin 2009 werd een overeenkomst gesloten om alle relevante werkzaamheden te combineren en JavaScript vooruit te helpen. Dit resulteerde in de release van de ECMAScript 5 Standard in december 2009.

## Hoe JS-bestanden te gebruiken ##

Om een JS-bestand te gebruiken, neemt u het op in het HTML-document. U gebruikt de link-tag om het bestand op te nemen, zoals hieronder wordt weergegeven.

```html
<script src="site.js"></script>
```

Het *src*-kenmerk van de *script*-tag bevat het pad naar het JS-bestand. Hierdoor wordt de JS-functionaliteit toegevoegd aan het HTML-document.

## JS-syntaxis ##

JavaScript-bestanden kunnen variabelen, operators, functies, voorwaarden, lussen, arrays, objecten, enz. bevatten. Hieronder vindt u een kort overzicht van de syntaxis van JavaScript.

- Elke opdracht eindigt met een puntkomma (;).
- Gebruik het sleutelwoord *var* om variabelen te declareren.
- Ondersteunt rekenkundige operatoren (+ - * / ) om waarden te berekenen.
- Opmerkingen van één regel worden toegevoegd met // en opmerkingen van meerdere regels worden omgeven door /* en */.
- Alle identifiers zijn hoofdlettergevoelig, dwz *modelNo* en *modelno* zijn twee verschillende variabelen.
- Functies worden gedefinieerd met het sleutelwoord *function*.
- Arrays kunnen worden gedefinieerd met vierkante haken [].
- JS ondersteunt vergelijkingsoperatoren zoals ==, != , >=, !==, etc.
- Klassen kunnen worden gedefinieerd met het sleutelwoord *class*.

## JS-gebruiksvoorbeeld ##

Het volgende toont een eenvoudig gebruiksvoorbeeld JavaScript-bestand.

### HTML-document ###

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

### JS-code ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referenties ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

