{
  "date": "2019-10-11",
  "keywords": [
"mng-tiedosto",
"mng-tiedostomuoto",
"mikä on mng-tiedosto",
"tiedosto",
"mng esimerkki",
"mng tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MNG-tiedostomuoto - Multiple Image Network Graphics File Format",
  "description": "Opi MNG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MNG-tiedostoja.",
  "linktitle": "MNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-mn-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on MNG-tiedosto?

Tiedosto, jonka pääte on .mng, on monikuvainen verkkografiikkatiedostomuoto, joka on samanlainen kuin [PNG](/image/png/)-kuvamuoto, mutta tukee animoituja kuvia. Se kehitettiin välttämään PNG-muodon ylikuormittamista animaatioiden lisäominaisuuksilla. MNG on myös samanlainen kuin [GIF](/image/gif/)-tiedostot, mutta käyttää enemmän pakkausta ja tukee täyttä alfa-ominaisuutta. MNG-tiedostojen epävirallinen MIME-mediatyyppi on video/x-mng. MNG-tiedostoja voidaan avata sovelluksissa, kuten ImageMagik ja IrfanView.

## MNG-tiedostomuoto

MNG-tiedostomuoto on samanlainen kuin PNG ja käyttää samaa lohkorakennetta kuin PNG-spesifikaatioissa on määritelty. MNG-dekooderin on kyettävä purkamaan PNG-tietovirrat määrittämättä mitään erityisiä lippuja dekoodausohjeille. MNG ryhmittelee useita kuvia yhteen kehykseksi, ja joitain kuvia käytetään spritenä paikasta toiseen siirtymiseen. Mekanismi mahdollistaa kuvatietojen uudelleenkäytön lähettämättä sitä uudelleen. {{HYPERLINKKI}} voidaan viitata kehittäjien tietoihin.

### MNG-allekirjoitus

MNG-tietovirta alkaa 8-tavuisella allekirjoituksella, joka sisältää:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Tämä on samanlainen kuin PNG-allekirjoitus, mutta sisältää MNG:tä PNG:n sijaan.

### MNG-kehys

MNG-kehys koostuu pienempien kuvien kaksiulotteisesta kuvasta. Jokaiseen pieneen kuvaan pääsee käsiksi rivi- ja sarakeindeksiyhdistelmällä. Muoto pystyy tallentamaan kolmiulotteisen vokseli-datan, joka on järjestetty sarjaan kaksiulotteisia tasoja. Jokaista tasoa edustaa PNG- tai Delta-PNG-tietovirta. Jokainen Delta-PNG-tietovirta määrittelee kuvan eroiksi PNG-emokuvasta. Tämä tarjoaa paljon kompaktimman tavan esittää seuraavat kuvat kuin käyttää täydellistä PNG-tietovirtaa kullekin.

## Viitteet ##

* [MNG](http://www.libpng.org/pub/mng/)

* [MNG-muoto v 1.0](http://www.libpng.org/pub/mng/spec/)


