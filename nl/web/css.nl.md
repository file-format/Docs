---
date: 2019-10-11
keywords: css, .css, css-bestandsindeling, hoe css-bestanden te openen, trapsgewijze stijlbladen
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS-bestandsindeling
linktitle: CSS
description: "Meer informatie over CSS-bestandsindelingen en API's die CSS-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Wat is een CSS-bestand? ##

CSS (Cascading Style Sheets) zijn bestanden die beschrijven hoe HTML-elementen worden weergegeven op het scherm, op papier, enz. Met HTML kunt u ofwel ingesloten stijlen hebben of stijlen kunnen worden gedefinieerd in een externe stylesheet. Voor het insluiten van de stijlen, de \ <style>\</style> labels worden gebruikt. De externe stylesheets worden opgeslagen in bestanden met de extensie .css. Met de externe CSS kunt u deze op meerdere HTML-pagina's opnemen om de stijl van die pagina's bij te werken. Zelfs een enkel CSS-bestand kan worden gebruikt om een complete website op te maken.

## Korte geschiedenis ##

CSS1 werd uitgebracht in 1996 met Bert Bos als co-auteur. De CSS-werkgroep begon te werken aan de problemen die niet aan bod kwamen in CSS1. Dit resulteerde in de creatie van CSS2 in november 1997, dat op 12 mei 1998 als W3C-aanbeveling werd gepubliceerd. Deze versie voegde ondersteuning toe voor mediaspecifieke apparaten zoals printers, downloadbare lettertypen, tabellen en elementpositionering. In juni 1999 werd CSS3 de aanbeveling van W3C. Dit verdeelde de documentatie in modules waarbij elke module uitbreidingsfuncties had die zijn gedefinieerd in CSS2.

## Hoe CSS-bestanden te gebruiken ##

Om een CSS-bestand te gebruiken, neemt u het op in de kopsectie van het HTML-document. U gebruikt de link-tag om het bestand op te nemen, zoals hieronder wordt weergegeven.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

het attribuut *href* van de link-tag bevat het pad naar het CSS-bestand. Door dit te doen, worden de toepasselijke stijlen in het meegeleverde CSS-bestand toegepast op het HTML-document.

## CSS-syntaxis ##

Een CSS-regel bestaat uit twee componenten, een selector en een declaratie. Een selector wijst naar een element in het HTML-document. Het kan een elementtag zijn, een klassenaam, een id-naam, meerdere tags die de hiërarchie weergeven, enz. Een declaratie bevat de stijldefinitie bestaande uit eigenschap en waarde. De eigenschap identificeert de eigenschap van het element dat u wilt wijzigen en de waarde definieert de nieuwe waarde. Elke CSS-regel kan meerdere declaraties hebben. Het volgende is een voorbeeld van een CSS-regel.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

In het bovenstaande voorbeeld hebben we de **h1** als selector die alle h1-tags in het HTML-document selecteert. De regel heeft twee declaraties, één voor font-weight en de andere voor kleur. *font-weight* en *color* zijn eigenschappen en *700* en *forestgreen* zijn respectievelijk hun waarden.

## CSS-gebruiksvoorbeeld ##

Het volgende toont het HTML-voorbeelddocument en de stylesheet die is gebruikt om het op te maken. De vergelijkingsafbeelding wordt ook toegevoegd om de gestileerde en gewone HTML-documenten te vergelijken

### HTML-document ###

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

### CSS-stijlblad ###

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

### Uitvoervergelijking ###

De linkerkant van de afbeelding toont het HTML-document zonder de toegepaste stijlen en de rechterkant toont het HTML-document met de toegepaste stijlen.

{{< figure src="../CssExample.jpg" alt="Voorbeeld afbeelding" >}}

## Referenties ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

