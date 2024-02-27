---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass Fil Format
linktitle: Sass
description: Ltjene om Sass filformat og API'er, der kan oprette og åbne Sass fils.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Hvad er SASS fil? ##

Sass (syntaktisk fantastiske style sheets) er et preprocessor-scriptsprog. Det kompileres i [CSS](/web/css/) og gemmes med .sass-udvidelsen. Sass består af to syntakser, den originale baseret på indrykninger, der bruger .sass-udvidelsen, og den nyere SCSS med blokformatering som CSS, der bruger .scss-udvidelsen.

## Hvorfor bruge Sass ##

Sass er virkelig nyttig til at vedligeholde stilarter, da det giver mange funktioner som introducerer variabler, indlejring, mixins, importer og vælgernedarvning, der gør arbejdet med stilarter sjovt.

## Sådan bruger du SASS-filer ##

SASS-filer er ikke inkluderet direkte i [HTML](/web/html/)-dokumentet, men konverteres snarere til CSS-filer, der er inkluderet i HTML-filer. Du kan installere Sass af dit system ved at følge instruktionerne på [Official Sass Site](https://sass-lang.com/install).

Sass kan konverteres til CSS ved enten at konvertere en allerede gemt SASS-fil eller ved at holde øje med ændringer og konvertere efterhånden som filen gemmes. Kommandoerne for begge er givet nedenfor.

### Konverter én gang ###

Den første parameter i kommandoen er SASS-kildefilen, og den anden parameter er output-CSS-filen.

```cmd
sass main.sass main.css
```

### Hold øje med ændringer ###

Ovenstående kommando kan køres med et ekstra *watch* flag, der holder kommandoen kørende, og så snart Sass-filen er gemt, genereres output CSS.

```cmd
sass --watch main.sass main.css
```

## Sass-syntaks ##

Sass understøtter variabler, nesting, mixins, import, selector-arv osv. Nedenfor er eksempler på disse funktioner.

### Variabler ###

Variabler kan bruges til at indstille genbrugelige oplysninger såsom primærfarve eller polstring for en knap. Dette kan vise sig nyttigt, hvis du i fremtiden skulle ændre disse oplysninger, du bare ændrer dem ét sted, og de opdaterer overalt.

**Frygt**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

### Nesting ###

CSS-vælgere kan indlejres på samme måde som HTML-hierarkiet. I det følgende eksempel er spændvidden indlejret inde i h1-blokken.

**Frygt**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Mixins bruges til at gruppere lignende egenskaber sammen, der bruges flere steder. Mixins understøtter også parametre.

**Frygt**

**Erklærer en blanding**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Brug af en blanding**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Udvid/arv kan vise sig at være nyttig i tilfælde, hvor egenskaberne for en vælger skal deles med en anden vælger. I eksemplet nedenfor tager *.error-notice*-vælgeren alle egenskaberne for *.error-text*-vælgeren og tilføjer kant- og udfyldningsegenskaber.

**Frygt**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

Importering kan være nyttig, hvis du strukturerer dine stilarter i forskellige filer baseret på funktionalitet eller enhver anden struktur, du følger. Du kan importere alle disse filer i en primær SASS-fil, der senere konverteres til CSS. Mens du importerer, behøver du ikke at angive filtypenavnet i importinstruktionen. Sass kompilerer alle SASS-filer direkte. For at undgå at importere filer, der skal kompileres direkte, kan du gøre dem til partialer ved at tilføje understregning(_) i starten af deres navn. Partialer importeres svarende til normale Sass-filer.

**Frygt**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Output-CSS'en vil have stilene fra alle de importerede filer.

## Referencer ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

