---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass faila formaat
linktitle: Sass
description: Lnopelniet par Sass faila formātu un API, kas var izveidot un atvērt Sass failus.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Kas ir SASS fails? ##

Sass (sintaktiski lieliskas stila lapas) ir priekšapstrādātāja skriptu valoda. Tas ir apkopots [CSS](/web/css/) un tiek saglabāts ar paplašinājumu .sass. Sass sastāv no divām sintaksēm: oriģinālā pamatā ir atkāpes, kurās tiek izmantots paplašinājums .sass, un jaunākā SCSS ar bloku formatējumu, piemēram, CSS, kas izmanto paplašinājumu .scss.

## Kāpēc izmantot Sass ##

Sass ir ļoti noderīgs stilu uzturēšanā, jo tas nodrošina daudzas funkcijas, piemēram, mainīgo ieviešanu, ligzdošanu, sajaukšanu, importēšanu un atlasītāju pārmantošanu, kas padara darbu ar stiliem jautru.

## Kā izmantot SASS failus ##

SASS faili nav tieši iekļauti [HTML](/web/html/) dokumentā, bet drīzāk tiek pārveidoti par CSS failiem, kas ir iekļauti HTML failos. Varat instalēt Sass savā sistēmā, izpildot norādījumus, kas sniegti vietnē [Official Sass Site](https://sass-lang.com/install).

Sass var konvertēt uz CSS, vai nu konvertējot jau saglabātu SASS failu, vai arī vērojot izmaiņas un konvertējot, kamēr fails tiek saglabāts. Abu komandas ir norādītas zemāk.

### Pārvērst vienreiz ###

Komandas pirmais parametrs ir avota SASS fails, bet otrais parametrs ir izvades CSS fails.

```cmd
sass main.sass main.css
```

### Skatīties izmaiņas ###

Iepriekš minēto komandu var palaist ar papildu *watch* karogu, kas nodrošina komandas darbību, un, tiklīdz tiek saglabāts Sass fails, tiek ģenerēts izvades CSS.

```cmd
sass --watch main.sass main.css
```

## Sass sintakse ##

Sass atbalsta mainīgos, ligzdošanu, mixins, importēšanu, selektora pārmantošanu utt. Tālāk ir sniegti šo funkciju piemēri.

### Mainīgie ###

Mainīgos var izmantot, lai iestatītu atkārtoti lietojamu informāciju, piemēram, pogas primāro krāsu vai polsterējumu. Tas var izrādīties noderīgi, ja nākotnē jums būs jāmaina šī informācija, jūs vienkārši mainīsit to vienā vietā, un tā tiek atjaunināta visur.

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

CSS atlasītājus var ligzdot līdzīgi HTML hierarhijai. Nākamajā piemērā span ir ligzdots blokā h1.

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

Miksīnus izmanto, lai grupētu līdzīgas īpašības, kas tiek izmantotas vairākās vietās. Mixins atbalsta arī parametrus.

**Sass**

**Sajaukšanas paziņošana**

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

**Izmantojot mikseri**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Paplašināšana/mantošana var izrādīties noderīga gadījumos, kad viena atlasītāja īpašības ir jādala ar citu atlasītāju. Tālāk esošajā piemērā atlasītājs *.error-notice* ņem visus *.error-text* atlasītāja rekvizītus un pievieno apmales un polsterējuma rekvizītus.

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

Importēšana var būt noderīga, ja strukturējat savus stilus dažādos failos, pamatojoties uz funkcionalitāti vai jebkuru citu struktūru, kurai sekojat. Jūs varat importēt visus šos failus primārajā SASS failā, kas vēlāk tiek pārveidots par CSS. Importējot, importēšanas instrukcijā nav jānorāda faila paplašinājums. Sass tieši apkopo visus SASS failus. Lai izvairītos no failu importēšanas, kas jākompilē tiešā veidā, varat tos padarīt daļējus, pievienojot pasvītrojumu (_) to nosaukuma sākumā. Daļēji tiek importēti līdzīgi parastajiem Sass failiem.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Izvades CSS būs stili no visiem importētajiem failiem.

## Atsauces Nr.

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

