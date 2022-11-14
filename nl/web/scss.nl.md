---
date: 2019-10-11
keywords: scss, .scss, scss-bestandsindeling, hoe scss-bestanden te openen, syntactisch geweldig stylesheet, css-preprocessor, sass
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS-bestandsindeling - Sass Cascading Style Sheet
linktitle: SCSS
description: "Meer informatie over SCSS-bestandsindelingen en API's die SCSS-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Wat is een SCSS-bestand? ##

SCSS is de tweede syntaxis van Sass (Syntactically Awesome Stylesheet) die haakjes gebruikt in plaats van inspringingen. SCSS is zo ontworpen dat een geldig CSS3-bestand ook een geldig SCSS-bestand is. SCSS-bestanden worden opgeslagen met de extensie .scss.

## Waarom SCSS gebruiken ##

Omdat de ontwerpen van websites steeds complexer worden, resulteert dit in grote [CSS](/nl/web/css/)-bestanden. Dergelijke bestanden zijn moeilijker te onderhouden. Hier komt SCSS om de hoek kijken. SCSS introduceert variabelen, nesting, mixins, imports en selector-overerving in CSS-ontwikkeling. Deze toevoegingen maken het werken met design een stuk leuker.

## Hoe SCSS-bestanden te gebruiken ##

SCSS-bestanden worden niet rechtstreeks opgenomen in het [HTML](/nl/web/html/)-document zoals CSS. In plaats daarvan worden SCSS-bestanden geconverteerd naar CSS-bestanden die zijn opgenomen in HTML-bestanden. Om SCSS op uw systeem te installeren, volgt u de instructies op de [Officiële Sass-site](https://sass-lang.com/install).
Om SCSS naar CSS te converteren, kunt u een reeds opgeslagen SCSS-bestand converteren of kijken naar wijzigingen en converteren terwijl het bestand wordt opgeslagen. De opdrachten voor beide worden hieronder gegeven.

### Eenmaal converteren ###

De eerste parameter is het SCSS-bronbestand en de tweede parameter is het CSS-uitvoerbestand.

```cmd
sass main.scss main.css
```

### Let op veranderingen ###

De opdracht heeft een extra *watch**-vlag die ervoor zorgt dat de opdracht actief blijft en zodra het SCSS-bestand is opgeslagen, wordt output-CSS gegenereerd.

```cmd
sass --watch main.scss main.css
```

## SCSS-syntaxis ##

SCSS ondersteunt variabelen, nesting, mixins, imports, selector-overerving, enz. Hieronder vindt u voorbeelden van deze functies.

### Variabelen ###

Door het gebruik van variabelen kunt u herbruikbare informatie instellen, zoals de primaire kleur of achtergrondkleur voor de opslagknop. Dit is handig als u die informatie moet wijzigen, u wijzigt deze gewoon op één locatie en wordt bijgewerkt waar deze ook wordt gebruikt.

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

U kunt de CSS-kiezers nesten die vergelijkbaar zijn met de hiërarchie van HTML. In het onderstaande voorbeeld is de overspanning genest in het h1-blok.

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

Mixins kunnen worden gebruikt om vergelijkbare eigenschappen te groeperen die op meerdere plaatsen samen worden gebruikt. U kunt ook parameters doorgeven aan mixins.

**SCSS**

**Een mix aangeven**

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

**Een mix gebruiken**

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

Extend/Overerving is handig in gevallen waarin de eigenschappen van een selector moeten worden gedeeld met een andere selector. In het onderstaande voorbeeld neemt de *.error-notice* selector alle eigenschappen van de *.error-text* selector en voegt rand- en opvuleigenschappen toe.

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

Importeren kan nuttig zijn bij het scheiden van zorgen. U kunt de stijlen zo verdelen dat de koptekststijlen in een apart bestand staan, de voettekststijlen in een apart bestand, alle kleurvariabelen die in de stijlen worden gebruikt in een apart bestand, enz. Met deze techniek kan de stijlen blijven georganiseerd. U importeert gewoon de bestanden in uw hoofd-SCSS-bestand zoals in het onderstaande voorbeeld. U hoeft de bestandsextensie niet op te geven in de importinstructie. Sass compileert alle SCSS-bestanden rechtstreeks. Om te voorkomen dat importbestanden direct worden gecompileerd, kunt u ze gedeeltelijk maken door onderstrepingsteken (_) voor hun naam toe te voegen. U kunt gedeeltelijke delen importeren die vergelijkbaar zijn met normale SCSS-bestanden zonder het onderstrepingsteken.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

De output-CSS heeft de stijlen van alle geïmporteerde bestanden.

## Referenties ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

