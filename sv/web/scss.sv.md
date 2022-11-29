---
date: 2019-10-11
keywords: scss, .scss, scss filformat, hur man öppnar scss-filer, syntaktisk fantastisk stilmall, css-förprocessor, sass
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS-filformat - Sass Cascading Style Sheet
linktitle: SCSS
description: "Lär dig om SCSS-filformat och API:er som kan skapa och öppna SCSS-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Vad är en SCSS fil? ##

SCSS är den andra syntaxen för Sass (Syntactically Awesome Stylesheet) som använder parenteser istället för indrag. SCSS utformades på ett sådant sätt att en giltig CSS3-fil också är en giltig SCSS-fil. SCSS-filer lagras med tillägget .scss.

## Varför använda SCSS ##

Eftersom designen av webbplatser blir komplex, vilket resulterar i stora [CSS](/sv/web/css/)-filer. Sådana filer är svårare att underhålla. Det är här SCSS kommer in. SCSS introducerar variabler, kapsling, mixins, importer och väljararv i CSS-utveckling. Dessa tillägg gör arbetet med design mycket roligare.

## Hur man använder SCSS-filer ##

SCSS-filer ingår inte direkt i [HTML](/sv/web/html/)-dokumentet som CSS. Istället konverteras SCSS-filer till CSS-filer som ingår i HTML-filer. För att installera SCSS på ditt system, följ instruktionerna på den [officiella Sass-webbplatsen](https://sass-lang.com/install).
För att konvertera SCSS till CSS kan du antingen konvertera en redan sparad SCSS-fil eller se efter ändringar och konvertera allt eftersom filen sparas. Kommandona för båda ges nedan.

### Konvertera en gång ###

Den första parametern är käll-SCSS-filen och den andra parametern är utdata-CSS-filen.

```cmd
sass main.scss main.css
```

### Se upp för ändringar ###

Kommandot har en extra *watch**-flagga som håller kommandot igång och så snart SCSS-filen har sparats genereras utdata-CSS.

```cmd
sass --watch main.scss main.css
```

## SCSS-syntax ##

SCSS stöder variabler, kapsling, mixins, importer, väljararv, etc. Nedan ges exempel på dessa funktioner.

### Variabler ###

Genom att använda variabler kan du ställa in återanvändbar information som primärfärg eller bakgrundsfärg för sparaknappen. Detta är användbart om du behöver ändra den informationen, du ändrar den bara på en plats och den uppdateras var den än används.

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

Du kan kapsla CSS-väljarna på samma sätt som HTML-hierarkin. I exemplet nedan är spännvidden kapslad inuti h1-blocket.

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

Mixins kan användas för att gruppera liknande egenskaper som används tillsammans på flera ställen. Du kan också skicka parametrar till mixins.

**SCSS**

**Deklarerar en mixin**

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

**Med en mixin**

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

Utöka/arv är användbart i fall där egenskaperna för en väljare behöver delas med en annan väljare. I exemplet nedan tar *.error-notice*-väljaren alla egenskaper för *.error-text*-väljaren och lägger till kant- och utfyllnadsegenskaper.

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

Importering kan vara användbart för att separera problem. Du kan dela upp stilarna på ett sådant sätt att sidhuvudsstilarna finns i en separat fil, sidfotsstilarna finns i en separat fil, alla färgvariabler som används i stilarna kan vara i en separat fil, etc. Med denna teknik kan stilar håller sig organiserade. Du importerar bara filerna i din SCSS-huvudfil som visas i exemplet nedan. Du behöver inte ange filtillägget i importinstruktionen. Sass kompilerar alla SCSS-filer direkt. För att undvika att importfiler kompileras direkt kan du göra dem till partiella delar genom att lägga till understreck(_) före namnet. Du kan importera partier som liknar vanliga SCSS-filer utan understreck.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Utdata-CSS kommer att ha stilarna från alla importerade filer.

## Referenser ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

