{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"tiedosto",
"laajennus",
"muoto",
"3D-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Your file format guide to know what is an FBX file and APIs that can create and open them.",
  "title": "FBX - FilmBox 3D File Format",
  "linktitle": "FBX",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-fbx"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on FBX-tiedosto?

FBX, FilmBox, on suosittu 3D-tiedostomuoto, jonka Kaydara kehitti alun perin MotionBuilderille. Autodesk Inc osti sen vuonna 2006, ja se on nyt yksi tärkeimmistä 3D-vaihtoformaateista, jota monet 3D-työkalut käyttävät. FBX on saatavilla sekä binääri- että ASCII-tiedostomuodossa. Formaatti luotiin mahdollistamaan digitaalisen sisällön luontisovellusten yhteentoimivuus. Käytettävissä on monia työkaluja muuntamiseen FBX-tiedostomuodosta/muotoon.

## FBX-tiedostomuoto - lisätietoja

FBX on patentoitu muoto, eikä sen binääritiedostomuodon tietoja ole saatavilla virallisesti. Autodesk tarjoaa C++ FBX SDK:n lukemista, kirjoittamista ja FBX-tiedostoksi muuntamista varten. Python-tuonti- ja -vientiskripti FBX:lle on saatavilla myös Blender-ohjelmistossa, joka ei käytä FBX SDK:ta.

### Tekstipohjainen tiedostorakenne

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* NodeType-tunniste (luokan nimi)

* Siihen liittyy useita ominaisuuksia, monikkoelementit ovat tavallisia primitiivisiä tietotyyppejä: ##float, integer, string## jne.

* Luettelo, joka sisältää solmut samassa muodossa (rekursiivisesti).


Ne voidaan esittää loogisesti seuraavasti:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Jotkut vakiosolmuista on määritelty implisiittisiksi luetteloiksi, joissa jokainen kohde koostuu sisäkkäisestä luettelosta. Jokaisen sovelluksen, joka aikoo käyttää FBX-geometriaa, on jäsennettävä tämä sisältö ja annettava sille hyödyllinen merkitys. Esimerkki tekstipohjaisesta FBX-tiedostosta on alla:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## FBX-tiedostojen binaaritiedostorakenne

Kuten aiemmin mainittiin, FBX-tiedostomuotomääritykset eivät ole julkisesti saatavilla FBX:lle. Koska Blender Foundation toteuttaa FBX-tiedostomuodon käyttämättä yrityksen toimittamaa SDK:ta, osa binääritiedostomuodon tiedoista on [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) osana sen toteutusta.

Binääritiedostojen rakenne noudattaa seuraavaa järjestystä:

* Otsikko

* Object Record

* Alatunniste


### FBX-otsikko

Tiedoston otsikkotiedot koostuvat 27 tavusta.

* Tavut 0 - 20: Kaydara FBX Binary \x00 (tiedosto-magic, 2 välilyöntiä lopussa, sitten NULL-pääte).

* Tavut 21–22: [0x1A, 0x00]## (tuntematon, mutta kaikki havaitut tiedostot näyttävät nämä tavut).

* Tavut 23 - 26: allekirjoittamaton int, versionumero. 7300 versiolle 7.3 esimerkiksi.


### Objektietue ###

Otsikkoa seuraa objektitietue, joka on täysi solmutietue, jolla on tyhjä nimi ja tyhjä ominaisuusluettelo. Se sisältää rekursiivisesti koko tiedostomuodostelman.

### Alatunniste ###

FBX Footer -osio sijaitsee tiedoston lopussa, jonka sisältöä ei tunneta.

## Tallennusmuodot ##

FBX-tiedoston tietueet luokitellaan seuraavasti:

* Node Records

* Kiinteistörekisterit


### Solmun tietuemuoto ###

Jokainen solmun tietuemuoto on nimetty ja sillä on seuraava muistiasettelu.


|Koko (tavuja)|Päivämäärätyyppi|Nimi
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NimiLen
|NimenPituus|merkki|Nimi
|?|?|Ominaisuus[n], jossa n = 0:PropertyListLen
|Valinnainen| |
|?|?|Sisäkkäinen luettelo
|13|uint8[]|nollatietue

missä:

* `EndOffset` on etäisyys tiedoston alusta solmutietueen loppuun (eli seuraavaksi tulevan tiedoston ensimmäinen tavu). Tätä voidaan käyttää helposti ohittamaan tuntemattomia tai ei vaadittuja tietueita.

* `NumProperties` on solmuun liittyvän arvotuplen ominaisuuksien lukumäärä. Sisäkkäistä luetteloa viimeisenä elementtinä ei lasketa omaisuudeksi.

* "PropertyListLen" on ominaisuusluettelon pituus. Tämä on ##NumProperties## ominaisuuksien tallentamiseen vaadittava koko, joka riippuu ominaisuuksien tietotyypistä.

* `NameLen` on objektin nimen pituus merkeissä. Ainoa tapaus, jossa tämä on 0, näyttää olevan huipputason luettelot.

* "Nimi" on objektin nimi. Nollapäätettä ei ole.

* "Ominaisuus[n]" on n:s ominaisuus. Katso muotoa kohdasta ominaisuus Tietueen muoto. Ominaisuudet kirjoitetaan peräkkäin ja ilman täyttöä.

* "NestedList" on sisäkkäinen luettelo, jonka olemassaolo ilmaistaan NULL-tietueella aivan lopussa.


Sisäkkäisen luettelomerkinnän olemassaolo voidaan määrittää tarkistamalla, onko EndOffsetin saavuttamiseen jäljellä tavuja. Jos näin on, seuraava objektitietue tulee lukea suoraan viimeisen ominaisuuden jälkeen. Objektitietue seuraa sitten 13 nollatavua, jotka sitten yhdistetään EndOffsetin kanssa. NULL-merkinnän tarkoitus tai vaatimus ei ole tiedossa, ja se voi viitata johonkin muotoominaisuuteen.

### Kiinteistötietueen muoto ###

Ominaisuustietue sisältää tietoja ominaisuuksista, jotka ovat osa Nodea. Ominaisuustietueella on seuraava muistiasetelma:


|Koko (tavuja)|Tietotyyppi|Nimi
--- | --- | ---
|1|merkki|Tyyppikoodi
|?|?|Data

TypeCode edustaa merkkikoodeja, jotka on järjestetty ryhmiin, jotka vaativat samanlaista käsittelyä. TypeCode-koodit voidaan luokitella seuraaviin tyyppeihin, ja TypeCode voi olla yksi näiden tyyppien merkkikoodeista.

#### Primitiiviset tyypit ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Primitiivisen skalaarityyppisen tietueen tiedot ovat täsmälleen arvon binääriesitys pikkutavujärjestyksessä.

#### Taulukkotyypit ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Array Type -tiedot ovat monimutkaisempia ja ovat seuraavassa rakenteessa.


|Koko (tavuja)|Tietotyyppi|Nimi
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Koodaus
|4|Uint32|Compressed Length
|?|?|Sisältö

### Erikoistyypit ###

Seuraavat ovat erikoistyyppien tyyppikoodit.

```
S: String
R: raw binary data
```

Molemmat tyyppikoodit esitetään seuraavasti:


|Koko (tavuja)|Tietotyyppi|Nimi
--- | --- | ---
|4|Uin32|Pituus
|Pituus| |

Merkkijono ei ole nollapääte, ja se voi hyvinkin sisältää \0 merkkiä (tätä käytetään itse asiassa joissakin FBX-ominaisuuksissa).

## Viitteet ##

* [FBX – Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [FBX-binaaritiedostomuodon tekniset tiedot](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)


