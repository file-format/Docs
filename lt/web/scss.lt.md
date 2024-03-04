---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS failo formatas – Sass Cascading Style Sheet
linktitle: SCSS
description: Luždirbti apie SCSS failo formatą ir API, kurios gali sukurti ir atidaryti SCSS failąs.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Kas yra SCSS failas? ##

SCSS yra antroji Sass sintaksė (Syntactically Awesome Stylesheet), kurioje vietoj įtraukų naudojami skliaustai. SCSS buvo sukurtas taip, kad galiojantis CSS3 failas taip pat būtų galiojantis SCSS failas. SCSS failai saugomi su plėtiniu .scss.

## Kodėl naudoti SCSS ##

Kadangi svetainių dizainas tampa sudėtingas, todėl susidaro dideli [CSS](/web/css/) failai. Tokius failus sunkiau prižiūrėti. Čia atsiranda SCSS. SCSS įveda kintamuosius, lizdus, mišinius, importavimą ir selektorių paveldėjimą kuriant CSS. Dėl šių priedų darbas su dizainu tampa daug įdomesnis.

## Kaip naudoti SCSS failus ##

SCSS failai nėra tiesiogiai įtraukti į [HTML](/web/html/) dokumentą, pvz., CSS. Vietoj to, SCSS failai konvertuojami į CSS failus, kurie yra įtraukti į HTML failus. Norėdami įdiegti SCSS savo sistemoje, vadovaukitės instrukcijomis, pateiktomis [Official Sass Site](https://sass-lang.com/install).
Norėdami konvertuoti SCSS į CSS, galite konvertuoti jau išsaugotą SCSS failą arba stebėti pakeitimus ir konvertuoti, kai failas išsaugomas. Abiejų komandos pateiktos žemiau.

### Konvertuoti vieną kartą ###

Pirmasis parametras yra šaltinio SCSS failas, o antrasis parametras yra išvesties CSS failas.

```cmd
sass main.scss main.css
```

### Stebėkite pokyčius ###

Komanda turi papildomą *watch** vėliavėlę, kuri palaiko komandą, o kai tik įrašomas SCSS failas, sugeneruojamas išvesties CSS.

```cmd
sass --watch main.scss main.css
```

## SCSS sintaksė ##

SCSS palaiko kintamuosius, lizdus, mišinius, importavimą, selektorių paveldėjimą ir tt Toliau pateikiami šių funkcijų pavyzdžiai.

### Kintamieji ###

Naudodami kintamuosius galite nustatyti pakartotinai naudojamą informaciją, pvz., pagrindinę arba fono spalvą išsaugojimo mygtukui. Tai naudinga, jei reikia pakeisti tą informaciją, tiesiog pakeisite ją vienoje vietoje ir ji atnaujinama visur, kur ji bus naudojama.

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

**Sukurtas CSS**

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

### Įdėjimas ###

Galite įdėti CSS parinkiklius, panašius į HTML hierarchiją. Toliau pateiktame pavyzdyje intervalas yra įdėtas h1 bloko viduje.

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

**Sukurtas CSS**

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

### Mišiniai ###

Mišiniai gali būti naudojami sugrupuoti panašias savybes, kurios naudojamos kartu keliose vietose. Taip pat galite perduoti parametrus miksams.

**SCSS**

**Mišinio paskelbimas**

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

**Naudojant maišytuvą**

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

**Sukurtas CSS**

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

### Prailginti ###

Išplėtimas/paveldėjimas naudingas tais atvejais, kai vieno parinkiklio savybėmis reikia dalytis su kitu parinkikliu. Toliau pateiktame pavyzdyje *.error-notice* parinkiklis perima visas *.error-text* parinkiklio ypatybes ir prideda kraštinės bei užpildymo ypatybes.

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

**Sukurtas CSS**

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

### Importuoti ###

Importavimas gali būti naudingas atskiriant problemas. Stilius galite suskirstyti taip, kad antraščių stiliai būtų atskirame faile, poraštės stiliai – atskirame faile, visi stiliuose naudojami spalvų kintamieji gali būti atskirame faile ir tt Naudojant šią techniką, stiliai išlieka tvarkingi. Tiesiog importuokite failus į pagrindinį SCSS failą, kaip parodyta toliau pateiktame pavyzdyje. Importavimo instrukcijoje failo plėtinio nurodyti nereikia. Sass tiesiogiai kompiliuoja visus SCSS failus. Kad nebūtų importuojami failai, kurie būtų kompiliuojami tiesiogiai, galite padaryti juos daliniais pridėdami pabraukimo brūkšnį (_) prieš jų pavadinimą. Galite importuoti dalis, panašias į įprastus SCSS failus, be pabraukimo.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Išvesties CSS turės stilius iš visų importuotų failų.

## Nuorodos Nr.

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

