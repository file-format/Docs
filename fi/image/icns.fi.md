{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"laajennus",
"tiedosto",
"muoto",
"kuva",
"Apple-kuvake",
"Mac käyttöjärjestelmä",
"Omena",
"Kuvake"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS - Applen kuvakekuva",
  "description": "Opi ICNS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ICNS-tiedostoja.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-fis"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on ICNS-tiedosto? ##

MacOS-ohjelmien käyttämää kuvakemuotoa kutsutaan ICNS-tiedostoksi. Se sallii 1- ja 8-bittiset alfakaistat ja tallentaa yhden tai useamman kuvan, joka on yleensä tehty [PNG](/image/png/)-asiakirjoista. Ohjelmakuvake macOS-selaimessa ja käyttöliittymässä näytetään ICNS-tiedostojen avulla.

Sijainnin perusteella samalla tyylikuvakkeella voi olla useita asetuksia. ICNS-muotoon on tehty lukuisia muutoksia ja se on kehittynyt niin pitkälle, että sitä voidaan nyt käyttää perustana erilaisille yhteensopiville formaateille. Tässä on joitain muita tärkeitä asioita, jotka sinun on tiedettävä:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource ja Mac OS icons Resource ovat joitain muita nimiä. 

* Kuvaketiedoissa käytetään resurssihaaran lähdettä.

* Useimmissa tapauksissa tiedosto sisältää useita kuvia. 1612 pikseliä neliö ja 1024, 512, 256, 128, 48, 32 ja 16 pikseliä neliö ovat tuettuja kuvakokoja.



## ICNS-tiedostomuoto ##

ICNS-datamuoto on kapseli yhdelle tai useammalle kuvalle, joka tukee 1-bittisiä taajuuksia ja lukuisia kuvatiloja.
Käyttöjärjestelmä voi muuttaa kuvakkeiden kuvien kokoa vaaditun näytön kokoiseksi. Suuremmat kuvakekuvat tallennetaan yleensä [JPEG](/image/jpeg/) 2000- tai [PNG](/image/png/)-tiedostoina. Sekä pakatut että pakkaamattomat ICNS-tiedostot ovat mahdollisia.

Otsikko ja binäärikuvaketiedot muodostavat ICNS-tiedoston rakenteen. Otsikko sisältää 8 tavua dataa, joista neljä on magic literaalia ja joista neljä on tiedoston pituus. Kunkin kuvakekuvan tyyppi ja koko tallennetaan kuvaketieto-osioon, jota seuraa binäärikuvadata. Kuvan koko määrittää binääriosion koon.

## Tekniset tiedot ##

### Otsikko ###

|Offset|Koko|Tavoite
---|---|---|
|0|4|Magic literal, täytyy olla icns (0x69, 0x63, 0x6e, 0x73)
|4|4|Tiedoston pituus tavuina, msb ensin


### Kuvaketiedot ###

|Offset|Koko|Tavoite
---|---|---|
|0|4|Kuvakkeen tyyppi
|4|4|Tiedon pituus tavuina (mukaan lukien tyyppi ja pituus), msb ensin
|8|Muuttuja|Kuvaketiedot

### Puristus ###

Pikselitiedot on pakattu jossain määrin. 32-bittiset (is32, il32, ih32, it32) ja ARGB (ic04, ic05) pikselit pakataan usein (kanavakohtaisesti) samalla tavalla kuin PackBits.

|Liidiarvo|Häntätavuja|Tulos (pakkaamaton)
---|---|---|
|0 - 127|1 - 128|1 - 128 tavua
|128 - 255|1 tavu|3 - 130 kopiota

## Viite ##

* [ICNS – Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


