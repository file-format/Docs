---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass failo formaat
linktitle: Sass
description: Luždirbti apie Sass failo formatą ir API, kurios gali sukurti ir atidaryti Sass failąs.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Kas yra SASS failas? ##

Sass (sintaksiškai nuostabūs stiliaus lapai) yra pirminio procesoriaus scenarijų kalba. Jis sukompiliuotas į [CSS](/web/css/) ir saugomas su plėtiniu .sass. Sass susideda iš dviejų sintaksių: originalioji, pagrįsta įtraukomis, naudojanti .sass plėtinį, ir naujesnė SCSS su blokiniu formatavimu, pvz., CSS, naudojanti .scss plėtinį.

## Kodėl verta naudoti Sass ##

Sass tikrai padeda išlaikyti stilius, nes suteikia daug funkcijų, tokių kaip kintamųjų įvedimas, įdėjimas, mišiniai, importavimas ir parinkiklio paveldėjimas, dėl kurių darbas su stiliais yra įdomus.

## Kaip naudoti SASS failus ##

SASS failai nėra tiesiogiai įtraukti į [HTML](/web/html/) dokumentą, o konvertuojami į CSS failus, kurie yra įtraukti į HTML failus. Galite įdiegti Sass savo sistemoje vadovaudamiesi instrukcijomis, pateiktomis [Official Sass Site](https://sass-lang.com/install).

Sass gali būti konvertuojamas į CSS konvertuojant jau išsaugotą SASS failą arba stebint pakeitimus ir konvertuojant, kai failas išsaugomas. Abiejų komandos pateiktos žemiau.

### Konvertuoti vieną kartą ###

Pirmasis komandos parametras yra šaltinio SASS failas, o antrasis parametras yra išvesties CSS failas.

```cmd
sass main.sass main.css
```

### Stebėkite pokyčius ###

Aukščiau pateiktą komandą galima paleisti naudojant papildomą *watch* vėliavėlę, kuri palaiko komandą, o kai tik išsaugomas Sass failas, sugeneruojamas išvesties CSS.

```cmd
sass --watch main.sass main.css
```

## Sass sintaksė ##

Sass palaiko kintamuosius, lizdus, mišinius, importavimą, selektorių paveldėjimą ir tt Toliau pateikiami šių funkcijų pavyzdžiai.

### Kintamieji ###

Kintamieji gali būti naudojami norint nustatyti pakartotinai naudojamą informaciją, pvz., pagrindinę spalvą arba mygtuko užpildą. Tai gali būti naudinga, jei ateityje reikės pakeisti tą informaciją, tiesiog pakeisite ją vienoje vietoje ir ji atnaujinama visur.

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

CSS parinkiklius galima įdėti panašiai kaip HTML hierarchijoje. Šiame pavyzdyje intervalas yra įdėtas h1 bloko viduje.

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

Mišiniai naudojami sugrupuoti panašias savybes, kurios naudojamos keliose vietose. Mišiniai taip pat palaiko parametrus.

**Sass**

**Mišinio paskelbimas**

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

**Naudojant maišytuvą**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Išplėtimas/paveldėjimas gali būti naudingas tais atvejais, kai vieno parinkiklio savybėmis reikia dalytis su kitu parinkikliu. Toliau pateiktame pavyzdyje *.error-notice* parinkiklis perima visas *.error-text* parinkiklio ypatybes ir prideda kraštinės bei užpildymo ypatybes.

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

Importavimas gali būti naudingas, jei stilius suskirstysite į skirtingus failus, atsižvelgdami į funkcionalumą ar bet kokią kitą struktūrą, kurią vadovaujatės. Visus šiuos failus galite importuoti į pirminį SASS failą, kuris vėliau konvertuojamas į CSS. Importuojant nereikia nurodyti failo plėtinio importavimo instrukcijoje. Sass tiesiogiai kompiliuoja visus SASS failus. Kad nebūtų importuojami failai, kurie būtų kompiliuojami tiesiogiai, galite juos paversti daliniais pridėdami pabraukimo brūkšnį (_) jų pavadinimo pradžioje. Daliniai failai importuojami panašiai kaip įprasti Sass failai.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Išvesties CSS turės stilius iš visų importuotų failų.

## Nuorodos Nr.

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

