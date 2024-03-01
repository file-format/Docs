---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS-tiedostolomakeat
linktitle: CSS
description: Ltienaa CSS-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata CSS-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Mikä on CSS-tiedosto? ##

CSS (Cascading Style Sheets) ovat tiedostoja, jotka kuvaavat, miten HTML-elementit näytetään näytöllä, paperilla jne. HTML:n avulla voit määrittää joko upotettuja tyylejä tai tyylejä voidaan määrittää ulkoiseen tyylitaulukkoon. Tyylien upottamista varten \ <style>\</style> tunnisteita käytetään. Ulkoiset tyylisivut tallennetaan tiedostoihin, joiden tunniste on .css. Ulkoisen CSS:n avulla voit sisällyttää sen useille HTML-sivuille päivittääksesi näiden sivujen tyylin. Jopa yhtä CSS-tiedostoa voidaan käyttää kokonaisen verkkosivuston tyyliin.

## Lyhyt historia ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Tämä johti CSS2:n luomiseen marraskuussa 1997, joka julkaistiin W3C:n suosituksena 12. toukokuuta 1998. Tämä versio lisäsi tuen mediakohtaisille laitteille, kuten tulostimille, ladattaville fonteille, taulukoille ja elementtien sijoittelulle. Kesäkuussa 1999 CSS3:sta tuli W3C:n suositus. Tämä jakoi dokumentaation moduuleiksi, joissa jokaisessa moduulissa oli CSS2:ssa määriteltyjä laajennusominaisuuksia.

## Kuinka käyttää CSS-tiedostoja ##

Jos haluat käyttää CSS-tiedostoa, sisällytä se HTML-dokumentin head-osioon. Käytät linkkitunnistetta sisällyttääksesi tiedoston alla olevan kuvan mukaisesti.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

linkkitunnisteen *href*-attribuutti sisältää polun CSS-tiedostoon. Näin toimitetun CSS-tiedoston sisältämiä soveltuvia tyylejä sovelletaan HTML-dokumenttiin.

## CSS-syntaksi ##

CSS-sääntö koostuu kahdesta osasta, valitsimesta ja ilmoituksesta. Valitsin osoittaa HTML-dokumentin elementtiin. Se voi olla joko elementtitunniste, luokan nimi, id-nimi, useita hierarkiaa osoittavia tunnisteita jne. Ilmoitus sisältää tyylimäärittelyn, joka koostuu ominaisuudesta ja arvosta. Ominaisuus identifioi sen elementin ominaisuuden, jota haluat muuttaa, ja arvo määrittää sen uuden arvon. Jokaisella CSS-säännöllä voi olla useita ilmoituksia. Seuraavassa on esimerkki CSS-säännöstä.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Yllä olevassa esimerkissä meillä on **h1** valitsimena, joka valitsee kaikki HTML-dokumentin h1-tunnisteet. Säännössä on kaksi ilmoitusta, yksi fontin painolle ja toinen värille. *font-weight* ja *color* ovat ominaisuuksia ja *700* ja *forestgreen* ovat niiden arvoja.

## CSS-käyttöesimerkki ##

Seuraavassa on esimerkki HTML-asiakirjasta ja sen tyylistämiseen käytetty tyylitaulukko. Vertailukuva lisätään myös tyyliteltyjen ja tavallisten HTML-dokumenttien vertailuun

### HTML-dokumentti ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS-tyylitaulukko ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Tuotoksen vertailu ###

Kuvan vasemmalla puolella näkyy HTML-dokumentti ilman tyylejä ja oikea puoli näyttää HTML-dokumentin tyyleineen.

{{< figure src="../CssExample.jpg" alt="Esimerkkikuva" >}}

## Viitteet ##

- {{HYPERLINKKI1}}

