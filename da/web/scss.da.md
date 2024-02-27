---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS-filformat - Sass Cascading Style Hunet
linktitle: SCSS
description: Ltjene om SCSS filformat og API'er, der kan oprette og åbne SCSS fils.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Hvad er en SCSS fil? ##

SCSS er den anden syntaks af Sass (Syntactically Awesome Stylesheet), der bruger parenteser i stedet for fordybninger. SCSS blev designet på en sådan måde, at en gyldig CSS3-fil også er en gyldig SCSS-fil. SCSS-filer gemmes med filtypenavnet .scss.

## Hvorfor bruge SCSS ##

Da design af websteder bliver komplekse, hvilket resulterer i store [CSS](/web/css/) filer. Sådanne filer er sværere at vedligeholde. Det er her, SCSS kommer ind i billedet. SCSS introducerer variabler, nesting, mixins, importer og selector-arv i CSS-udvikling. Disse tilføjelser gør arbejdet med design meget sjovere.

## Sådan bruger du SCSS-filer ##

SCSS-filer er ikke inkluderet direkte i [HTML](/web/html/)-dokumentet som CSS. I stedet konverteres SCSS-filer til CSS-filer, der er inkluderet i HTML-filer. For at installere SCSS på dit system skal du følge instruktionerne på [Official Sass Site](https://sass-lang.com/install).
For at konvertere SCSS til CSS kan du enten konvertere en allerede gemt SCSS-fil eller se efter ændringer og konvertere, efterhånden som filen gemmes. Kommandoerne for begge er givet nedenfor.

### Konverter én gang ###

Den første parameter er kilde-SCSS-filen, og den anden parameter er output-CSS-filen.

```cmd
sass main.scss main.css
```

### Hold øje med ændringer ###

Kommandoen har et ekstra *watch**-flag, der holder kommandoen kørende, og så snart SCSS-filen er gemt, genereres output-CSS.

```cmd
sass --watch main.scss main.css
```

## SCSS-syntaks ##

SCSS understøtter variabler, nesting, mixins, import, selector-arv osv. Nedenstående er eksempler på disse funktioner.

### Variabler ###

Ved at bruge variabler kan du indstille genbrugelige oplysninger såsom primærfarve eller baggrundsfarve for knappen Gem. Dette er nyttigt, hvis du har brug for at ændre disse oplysninger, du ændrer dem bare ét sted, og de opdaterer, hvor end de bruges.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Genereret CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Indlejring ###

Du kan indlejre CSS-vælgerne svarende til HTML-hierarkiet. I eksemplet nedenfor er spændvidden indlejret inde i h1-blokken.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Genereret CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Mixins ###

Mixins kan bruges til at gruppere lignende egenskaber sammen, som bruges sammen flere steder. Du kan også sende parametre til mixins.

**SCSS**

**Erklærer en blanding**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Brug af en blanding**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**Genereret CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Forlænge ###

Udvid/arv er nyttig i tilfælde, hvor egenskaberne for en vælger skal deles med en anden vælger. I eksemplet nedenfor tager *.error-notice*-vælgeren alle egenskaberne for *.error-text*-vælgeren og tilføjer kant- og udfyldningsegenskaber.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**Genereret CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Importer ###

Importering kan være nyttig til adskillelse af bekymringer. Du kan opdele stilene på en sådan måde, at sidehovedstilene er i en separat fil, sidefodstilene er i en separat fil, alle farvevariablerne, der bruges i stilene, kan være i en separat fil osv. Ved at bruge denne teknik kan stilarter forbliver organiseret. Du importerer bare filerne i din SCSS-hovedfil som vist i eksemplet nedenfor. Du behøver ikke at angive filtypenavnet i importinstruktionen. Sass kompilerer alle SCSS-filer direkte. For at undgå at importere filer, der skal kompileres direkte, kan du gøre dem til partialer ved at tilføje understregning(_) før deres navn. Du kan importere partialer svarende til normale SCSS-filer uden understregning.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Output-CSS'en vil have stilene fra alle de importerede filer.

## Referencer ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

