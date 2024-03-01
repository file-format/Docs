---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS-tiedostomuoto - Sass Cascading Style Sheet
linktitle: SCSS
description: Ltienaa SCSS-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata SCSS-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Mikä on SCSS-tiedosto? ##

SCSS on Sassin (Syntactically Awesome Stylesheet) toinen syntaksi, joka käyttää sulkuja sisennysten sijaan. SCSS on suunniteltu siten, että kelvollinen CSS3-tiedosto on myös kelvollinen SCSS-tiedosto. SCSS-tiedostot tallennetaan .scss-tunnisteella.

## Miksi käyttää SCSS:ää ##

Koska verkkosivustojen suunnittelu on tulossa monimutkaiseksi, mikä johtaa suuriin [CSS](/web/css/)-tiedostoihin. Tällaisia tiedostoja on vaikeampi ylläpitää. Tässä SCSS tulee käyttöön. SCSS tuo CSS-kehityksessä muuttujat, sisäkkäiset, sekoitukset, tuonnit ja valitsimien periytymisen. Nämä lisäykset tekevät suunnittelun parissa työskentelemisestä paljon hauskempaa.

## Kuinka käyttää SCSS-tiedostoja ##

SCSS-tiedostot eivät sisälly suoraan [HTML](/web/html/)-dokumenttiin, kuten CSS. Sen sijaan SCSS-tiedostot muunnetaan CSS-tiedostoiksi, jotka sisältyvät HTML-tiedostoihin. Asenna SCSS järjestelmääsi noudattamalla sivulla [Official Sass Site](https://sass-lang.com/install) annettuja ohjeita.
Jos haluat muuntaa SCSS:n CSS:ksi, voit joko muuntaa jo tallennetun SCSS-tiedoston tai seurata muutoksia ja muuntaa tiedostoa tallennettaessa. Molempien komennot on annettu alla.

### Muunna kerran ###

Ensimmäinen parametri on lähde-SCSS-tiedosto ja toinen parametri on tuloste CSS-tiedosto.

```cmd
sass main.scss main.css
```

### Varo muutoksia ###

Komennossa on ylimääräinen *watch**-lippu, joka pitää komennon käynnissä ja heti kun SCSS-tiedosto on tallennettu, CSS-tuloste luodaan.

```cmd
sass --watch main.scss main.css
```

## SCSS-syntaksi ##

SCSS tukee muuttujia, sisäkkäisyyttä, mixinejä, tuontia, valitsimen periytymistä jne. Alla on esimerkkejä näistä ominaisuuksista.

### Muuttujat ###

Muuttujien avulla voit asettaa tallennuspainikkeelle uudelleenkäytettäviä tietoja, kuten päävärin tai taustavärin. Tämä on hyödyllistä, jos sinun on muutettava tietoja, muutat niitä vain yhdessä paikassa ja ne päivittyvät aina, kun niitä käytetään.

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

**Luotu CSS**

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

### Pesintä ###

Voit sijoittaa CSS-valitsimet samankaltaisesti kuin HTML-hierarkia. Alla olevassa esimerkissä jänneväli on sisäkkäin h1-lohkon sisällä.

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

**Luotu CSS**

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

Miksiineillä voidaan ryhmitellä samanlaisia ominaisuuksia, joita käytetään yhdessä useissa paikoissa. Voit myös välittää parametreja mixineille.

**SCSS**

**sekoituksen ilmoittaminen**

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

**Mixinin käyttäminen**

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

**Luotu CSS**

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

### Laajenna ###

Laajenna/Periytys on hyödyllinen tapauksissa, joissa yhden valitsimen ominaisuudet on jaettava toisen valitsimen kanssa. Alla olevassa esimerkissä *.error-notice*-valitsin ottaa kaikki *.error-text*-valitsimen ominaisuudet ja lisää reuna- ja täyteominaisuudet.

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

**Luotu CSS**

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

### Tuonti ###

Tuonti voi olla hyödyllistä huolenaiheiden erottamisessa. Voit jakaa tyylit siten, että otsikotyylit ovat erillisessä tiedostossa, alatunnistyylit erillisessä tiedostossa, kaikki tyyleissä käytetyt värimuuttujat voivat olla erillisessä tiedostossa jne. Tätä tekniikkaa käyttämällä tyylit pysyvät järjestyksessä. Tuot vain pää-SCSS-tiedostosi tiedostot alla olevan esimerkin mukaisesti. Sinun ei tarvitse määrittää tiedostotunnistetta tuontiohjeessa. Sass kokoaa kaikki SCSS-tiedostot suoraan. Välttääksesi tuontitiedostojen käännöksen suoraan, voit tehdä niistä osittaisia lisäämällä alaviivan (_) niiden nimeen. Voit tuoda tavallisia SCSS-tiedostoja muistuttavia osia ilman alaviivaa.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Tulostetussa CSS:ssä on kaikkien tuotujen tiedostojen tyylit.

## Viitteet ##

- {{HYPERLINKKI}})
- {{HYPERLINKKI1}}

