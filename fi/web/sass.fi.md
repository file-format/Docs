---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass tiedostolomakeat
linktitle: Sass
description: Lansaita Sass-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata Sass-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Mikä on SASS-tiedosto? ##

Sass (syntaktisesti mahtavat tyylisivut) on esiprosessorin komentosarjakieli. Se on käännetty tiedostoon {{HYPERLINKKI}} ja tallennetaan .sass-laajennuksella. Sass koostuu kahdesta syntaksista, alkuperäinen perustuu sisennyksiin, jotka käyttävät .sass-laajennusta, ja uudempi SCSS, jossa on lohkomuotoilu, kuten CSS, joka käyttää .scss-laajennusta.

## Miksi käyttää Sassia ##

Sass on todella hyödyllinen tyylien ylläpitämisessä, sillä se tarjoaa monia ominaisuuksia, kuten muuttujien esittelyn, sisäkkäisyyden, sekoitukset, tuonti- ja valitsimen periytymisen, jotka tekevät tyylien kanssa työskentelystä hauskaa.

## Kuinka käyttää SASS-tiedostoja ##

SASS-tiedostoja ei sisällytetä suoraan [HTML](/web/html/)-dokumenttiin, vaan ne muunnetaan CSS-tiedostoiksi, jotka sisältyvät HTML-tiedostoihin. Voit asentaa Sassin järjestelmästäsi noudattamalla {{HYPERLINKKI}}:ssa annettuja ohjeita.

Sass voidaan muuntaa CSS:ksi joko muuntamalla jo tallennettu SASS-tiedosto tai tarkkailemalla muutoksia ja muuntamalla tiedostoa tallennettaessa. Molempien komennot on annettu alla.

### Muunna kerran ###

Komennon ensimmäinen parametri on lähde-SASS-tiedosto ja toinen parametri on tuloste CSS-tiedosto.

```cmd
sass main.sass main.css
```

### Varo muutoksia ###

Yllä oleva komento voidaan suorittaa ylimääräisellä *watch*-lipulla, joka pitää komennon käynnissä ja heti kun Sass-tiedosto on tallennettu, CSS-tulostus luodaan.

```cmd
sass --watch main.sass main.css
```

## Sass-syntaksi ##

Sass tukee muuttujia, sisäkkäisyyttä, mixinejä, tuontia, valitsimen periytymistä jne. Alla on esimerkkejä näistä ominaisuuksista.

### Muuttujat ###

Muuttujia voidaan käyttää uudelleenkäytettävien tietojen, kuten painikkeen päävärin tai pehmusteen, asettamiseen. Tämä voi osoittautua hyödylliseksi, jos joudut tulevaisuudessa muuttamaan tietoja, muutat niitä vain yhdessä paikassa ja ne päivittyvät kaikkialle.

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

CSS-valitsimet voidaan upottaa HTML-hierarkian tapaan. Seuraavassa esimerkissä jänneväli on sisäkkäin h1-lohkon sisällä.

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

Miksiineillä ryhmitellään yhteen samanlaisia ominaisuuksia, joita käytetään useissa paikoissa. Mixiinit tukevat myös parametreja.

**Sass**

**sekoituksen ilmoittaminen**

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

**Mixinin käyttäminen**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Laajentaminen/perintö voi osoittautua hyödylliseksi tapauksissa, joissa yhden valitsimen ominaisuudet on jaettava toisen valitsimen kanssa. Alla olevassa esimerkissä *.error-notice*-valitsin ottaa kaikki *.error-text*-valitsimen ominaisuudet ja lisää reuna- ja täyteominaisuudet.

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

Tuominen voi olla hyödyllistä, jos strukturoit tyylisi erilaisiksi tiedostoiksi toiminnallisuuden tai muun noudattamasi rakenteen perusteella. Voit tuoda kaikki nämä tiedostot ensisijaiseen SASS-tiedostoon, joka muunnetaan myöhemmin CSS:ksi. Tuonnin aikana sinun ei tarvitse määrittää tiedostotunnistetta tuontiohjeessa. Sass kokoaa kaikki SASS-tiedostot suoraan. Voit välttää tuontitiedostojen käännöksen suoraan tekemällä niistä osittaisia lisäämällä alaviivan (_) niiden nimen alkuun. Osat tuodaan samalla tavalla kuin tavalliset Sass-tiedostot.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Tulostettavassa CSS:ssä on kaikkien tuotujen tiedostojen tyylit.

## Viitteet ##

- {{HYPERLINKKI}})
- {{HYPERLINKKI1}}

