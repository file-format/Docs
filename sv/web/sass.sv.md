---
date: 2019-10-11
keywords: sass, .sass, sass-filformat, hur man öppnar sass-filer, syntaktisk fantastisk stilmall, css-förprocessor, sass
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass filformat
linktitle: Sass
description: "Lär dig om Sass-filformat och API:er som kan skapa och öppna Sass-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Vad är SASS fil? ##

Sass (syntaktiskt häftiga stilmallar) är ett preprocessor-skriptspråk. Den kompileras till [CSS](/sv/web/css/) och lagras med tillägget .sass. Sass består av två syntaxer, den ursprungliga baserad på indrag som använder tillägget .sass och den nyare SCSS med blockformatering som CSS som använder tillägget .scss.

## Varför använda Sass ##

Sass är verkligen till hjälp för att underhålla stilar eftersom det ger många funktioner som introducerar variabler, kapsling, mixins, importer och väljararv som gör det roligt att arbeta med stilar.

## Hur man använder SASS-filer ##

SASS-filer ingår inte direkt i [HTML](/sv/web/html/)-dokumentet utan konverteras snarare till CSS-filer som ingår i HTML-filer. Du kan installera Sass av ditt system genom att följa instruktionerna på den [officiella Sass webbplats](https://sass-lang.com/install).

Sass kan konverteras till CSS genom att antingen konvertera en redan sparad SASS-fil eller genom att se efter ändringar och konvertera allt eftersom filen sparas. Kommandona för båda ges nedan.

### Konvertera en gång ###

Den första parametern i kommandot är SASS-källfilen och den andra parametern är utdata-CSS-filen.

```cmd
sass main.sass main.css
```

### Se upp för ändringar ###

Ovanstående kommando kan köras med en extra *watch*-flagga som håller kommandot igång och så fort Sass-filen har sparats genereras utdata-CSS.

```cmd
sass --watch main.sass main.css
```

## Sass Syntax ##

Sass stöder variabler, kapsling, mixins, importer, väljararv, etc. Nedan ges exempel på dessa funktioner.

### Variabler ###

Variabler kan användas för att ställa in återanvändbar information som primärfärg eller stoppning för en knapp. Detta kan vara användbart om du i framtiden behövde ändra den informationen, du bara ändrar den på en plats och den uppdateras överallt.

**Sass**

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

**Genererad CSS**

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

CSS-väljare kan kapslas på samma sätt som HTML-hierarkin. I följande exempel är intervallet kapslat inuti h1-blocket.

**Sass**

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

**Genererad CSS**

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

Mixins används för att gruppera liknande egenskaper som används på flera ställen. Mixins stöder också parametrar.

**Sass**

**Deklarerar en mixin**

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

**Med en mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Genererad CSS**

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

### Förläng ###

Extend/Arv kan visa sig vara användbart i de fall då egenskaperna för en väljare behöver delas med en annan väljare. I exemplet nedan tar *.error-notice*-väljaren alla egenskaper för *.error-text*-väljaren och lägger till kant- och utfyllnadsegenskaper.

**Sass**

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

**Genererad CSS**

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

### Importera ###

Importering kan vara användbart om du strukturerar dina stilar i olika filer baserat på funktionalitet eller någon annan struktur som du följer. Du kan importera alla dessa filer i en primär SASS-fil som senare konverteras till CSS. När du importerar behöver du inte ange filtillägget i importinstruktionen. Sass kompilerar alla SASS-filer direkt. För att undvika att importera filer som ska kompileras direkt kan du göra dem till partiella delar genom att lägga till understreck(_) i början av namnet. Partier importeras på samma sätt som vanliga Sass-filer.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Utdata-CSS kommer att ha stilarna från alla importerade filer.

## Referenser ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

