---
date: 2019-10-11
keywords: sass, .sass, sass-bestandsindeling, hoe sass-bestanden te openen, syntactisch geweldig stylesheet, css-preprocessor, sass
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass-bestandsindeling
linktitle: Sass
description: "Meer informatie over Sass-bestandsindeling en API's die Sass-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Wat is een SASS-bestand? ##

Sass (syntactisch geweldige stylesheets) is een preprocessor-scripttaal. Het wordt gecompileerd in [CSS](/nl/web/css/) en wordt opgeslagen met de .sass-extensie. Sass bestaat uit twee syntaxis, het origineel is gebaseerd op inspringingen die de .sass-extensie gebruiken en de nieuwere SCSS met blokopmaak zoals CSS die de .scss-extensie gebruikt.

## Waarom Sass gebruiken ##

Sass is erg handig bij het onderhouden van stijlen, omdat het veel functies biedt, zoals het introduceren van variabelen, nesten, mixins, imports en selector-overerving die het werken met stijlen leuk maken.

## SASS-bestanden gebruiken ##

SASS-bestanden worden niet rechtstreeks in het [HTML](/nl/web/html/)-document opgenomen, maar worden eerder geconverteerd naar CSS-bestanden die in HTML-bestanden zijn opgenomen. U kunt Sass van uw systeem installeren door de instructies op de [Officiële Sass-site](https://sass-lang.com/install) te volgen.

Sass kan worden geconverteerd naar CSS door een reeds opgeslagen SASS-bestand te converteren of door te letten op wijzigingen en te converteren terwijl het bestand wordt opgeslagen. De opdrachten voor beide worden hieronder gegeven.

### Eenmaal converteren ###

De eerste parameter van de opdracht is het SASS-bronbestand en de tweede parameter is het CSS-uitvoerbestand.

```cmd
sass main.sass main.css
```

### Let op veranderingen ###

De bovenstaande opdracht kan worden uitgevoerd met een extra *watch*-vlag die de opdracht actief houdt en zodra het Sass-bestand is opgeslagen, wordt output-CSS gegenereerd.

```cmd
sass --watch main.sass main.css
```

## Sass-syntaxis ##

Sass ondersteunt variabelen, nesting, mixins, imports, selector-overerving, enz. Hieronder vindt u voorbeelden van deze functies.

### Variabelen ###

Variabelen kunnen worden gebruikt om herbruikbare informatie in te stellen, zoals de primaire kleur of opvulling voor een knop. Dit kan handig zijn als u in de toekomst die informatie moet wijzigen, u deze op één locatie wijzigt en overal wordt bijgewerkt.

**Sas**

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

**Gegenereerde CSS**

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

### Nesten ###

CSS-selectors kunnen worden genest, vergelijkbaar met de hiërarchie van HTML. In het volgende voorbeeld is de overspanning genest in het h1-blok.

**Sas**

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

**Gegenereerde CSS**

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

Mixins worden gebruikt om vergelijkbare eigenschappen te groeperen die op meerdere plaatsen worden gebruikt. Mixins ondersteunen ook parameters.

**Sas**

**Een mix aangeven**

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

**Een mix gebruiken**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Gegenereerde CSS**

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

### Verlengen ###

Extend/Overerving kan nuttig zijn in gevallen waarin de eigenschappen van een selector moeten worden gedeeld met een andere selector. In het onderstaande voorbeeld neemt de *.error-notice* selector alle eigenschappen van de *.error-text* selector en voegt rand- en opvuleigenschappen toe.

**Sas**

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

**Gegenereerde CSS**

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

### Importeren ###

Importeren kan handig zijn als u uw stijlen in verschillende bestanden structureert op basis van functionaliteit of een andere structuur die u volgt. U kunt al deze bestanden importeren in een primair SASS-bestand dat later wordt geconverteerd naar CSS. Tijdens het importeren hoeft u de bestandsextensie niet op te geven in de importinstructie. Sass compileert alle SASS-bestanden rechtstreeks. Om te voorkomen dat importbestanden direct worden gecompileerd, kunt u ze gedeeltelijk maken door onderstrepingsteken (_) toe te voegen aan het begin van hun naam. Gedeelten worden geïmporteerd op dezelfde manier als normale Sass-bestanden.

**Sas**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

De output-CSS heeft de stijlen van alle geïmporteerde bestanden.

## Referenties ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

