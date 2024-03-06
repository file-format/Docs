---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS faila formāts — Sass Cascading Style Sheet
linktitle: SCSS
description: Lnopelniet par SCSS faila formātu un API, kas var izveidot un atvērt SCSS failus.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Kas ir SCSS fails? ##

SCSS ir Sass (sintaktiski satriecoša stila lapas) otrā sintakse, kurā tiek izmantotas iekavas, nevis atkāpes. SCSS tika izstrādāts tā, lai derīgs CSS3 fails būtu arī derīgs SCSS fails. SCSS faili tiek glabāti ar paplašinājumu .scss.

## Kāpēc izmantot SCSS ##

Tā kā vietņu dizains kļūst sarežģīts, kā rezultātā tiek izveidoti lieli [CSS](/web/css/) faili. Šādus failus ir grūtāk uzturēt. Šeit parādās SCSS. SCSS ievieš mainīgos lielumus, ligzdošanu, mixins, importēšanu un selektora pārmantošanu CSS izstrādē. Šie papildinājumi padara darbu ar dizainu daudz jautrāku.

## Kā lietot SCSS failus ##

SCSS faili nav tieši iekļauti [HTML](/web/html/) dokumentā, piemēram, CSS. Tā vietā SCSS faili tiek pārveidoti par CSS failiem, kas ir iekļauti HTML failos. Lai instalētu SCSS savā sistēmā, izpildiet norādījumus, kas sniegti vietnē [Official Sass Site](https://sass-lang.com/install).
Lai pārvērstu SCSS par CSS, varat konvertēt jau saglabātu SCSS failu vai arī skatīties izmaiņas un konvertēt, kad fails tiek saglabāts. Abu komandas ir norādītas tālāk.

### Pārvērst vienreiz ###

Pirmais parametrs ir avota SCSS fails, bet otrais parametrs ir izejas CSS fails.

```cmd
sass main.scss main.css
```

### Skatīties izmaiņas ###

Komandai ir papildu karodziņš *watch**, kas nodrošina komandas darbību, un, tiklīdz tiek saglabāts SCSS fails, tiek ģenerēts izvades CSS.

```cmd
sass --watch main.scss main.css
```

## SCSS sintakse ##

SCSS atbalsta mainīgos lielumus, ligzdošanu, mixins, importēšanu, selektora pārmantošanu utt. Tālāk ir sniegti šo līdzekļu piemēri.

### Mainīgie ###

Izmantojot mainīgos, varat iestatīt atkārtoti lietojamu informāciju, piemēram, saglabāšanas pogas primāro krāsu vai fona krāsu. Tas ir noderīgi, ja jums ir jāmaina šī informācija, vienkārši mainiet to vienā vietā, un tā tiek atjaunināta visur, kur tā tiek izmantota.

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

**Ģenerēts CSS**

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

### Ligzdošana ###

Varat ligzdot CSS atlasītājus līdzīgi HTML hierarhijai. Tālāk sniegtajā piemērā span ir ligzdots blokā h1.

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

**Ģenerēts CSS**

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

Mixins var izmantot, lai grupētu līdzīgas īpašības, kas tiek izmantotas kopā vairākās vietās. Varat arī nodot parametrus mixiniem.

**SCSS**

**Sajaukšanas paziņošana**

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

**Izmantojot mikseri**

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

**Ģenerēts CSS**

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

### Pagarināt ###

Paplašināšana/mantošana ir noderīga gadījumos, kad viena atlasītāja īpašības ir jādala ar citu atlasītāju. Tālāk esošajā piemērā *.error-notice* atlasītājs ņem visus *.error-text* atlasītāja rekvizītus un pievieno apmales un polsterējuma rekvizītus.

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

**Ģenerēts CSS**

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

### Importēt ###

Importēšana var būt noderīga problēmu nošķiršanā. Jūs varat sadalīt stilus tā, lai galvenes stili atrodas atsevišķā failā, kājenes stili atrodas atsevišķā failā, visi stilos izmantotie krāsu mainīgie var būt atsevišķā failā utt. Izmantojot šo paņēmienu, stili paliek sakārtoti. Jūs vienkārši importējiet failus savā galvenajā SCSS failā, kā parādīts tālāk esošajā piemērā. Importēšanas instrukcijā faila paplašinājums nav jānorāda. Sass tieši apkopo visus SCSS failus. Lai izvairītos no failu importēšanas, kas jākompilē tiešā veidā, varat tos padarīt daļējus, pirms to nosaukuma pievienojot pasvītrojumu (_). Varat importēt daļējas daļas, kas līdzīgas parastajiem SCSS failiem bez pasvītras.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Izvades CSS būs stili no visiem importētajiem failiem.

## Atsauces Nr.

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

