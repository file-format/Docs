{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Tiedosto muoto",
"Avata",
"Lukea",
"Luoda",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi HPGL-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata HPGL-tiedostoja.",
  "title": "HPGL-tiedostomuoto – opi tiedostomuoto-asiantuntijoilta!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-fil"
}
},
  "lastmod": "2020-07-28"
}

## Mikä on HPGL-tiedosto?

HPGFL (Hewlett-Packard Graphics Language) -tiedosto sisältää ohjejoukon HP:n kehittämää piirturiohjausta varten. HP-plotterit käyttävät tätä tiedostoa vektori- ja rasterisisällön piirtämiseen ja tulostamiseen paperille.

### HPGL-komento

HPGL-komento koostuu seuraavista.
 * Kahden merkin aakkosten komento-osa
 * Parametriosio
 * Terminaattori-osio

Jokainen tiedoston parametri on erotettava erottimella, jos parametreja on useita.

### HPGL-komentoesimerkki

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinaattijärjestelmä

Koordinaattijärjestelmät koostuvat 2-ulotteisista mittausindikaattoreista minkä tahansa tietyn sijainnin paikantamiseksi. HPGL käyttää tähän tarkoitukseen sekä Piirturi- että käyttäjän koordinaattijärjestelmää.

#### Piirturikoordinaattijärjestelmä

Tätä koordinaattijärjestelmää käytetään piirustuksen piirtämiseen, joka perustuu plotterin liikkeeseen. Tyypillinen plotterin minimiliikkeen XY-yksikkö on 0,025 mm. Mahdollinen piirustusalue muuttuu plotterityyppien mukaan.

#### Käyttäjän koordinaattijärjestelmä

Käyttäjän määrittelemä koordinaattijärjestelmä voidaan määrittää mittakaavan ja origon avulla. Nämä muunnetaan piirturikoordinaateiksi käyttämällä IP-komentoa ja SC-komentoa. Plotterijärjestelmän koordinaatteja käytetään oletusarvoisesti, jos tätä muuntamista ei suoriteta.

## HPGL-tiedostomuoto
HPGL-tiedostot ovat ASCII (tekstitiedosto) -muodossa ja alkavat muutamalla asennuskomennolla. Tämä asettaa piirturille tietyt parametrit piirtämistä varten. Tyypillinen HPGL-tiedosto näyttää seuraavalta.

|Komento|Merkitys
---|---|
|IN;|alusta, aloita piirustustyö|
|IP;|asettaa skaalauspisteet (P1 ja P2) oletusasemiinsa|
|SP1;|valitse kynä 1|
|PU0,0;|nosta kynä ylös ja siirry seuraavan toimenpiteen aloituspisteeseen|
|PD100,0,100,100,0,100,0,0;|laita kynä alas ja siirry seuraaviin paikkoihin (piirrä laatikko sivun ympärille)|
|PU50,50;|Kynä ylös ja siirry X,Y-koordinaatteihin 50,50|
|CI25;|piirrä ympyrä, jonka säde on 25|
|SS;|valitse vakiomerkkisarja|
|DT*,1;|aseta tekstin erotin tähdeksi, äläkä tulosta niitä (1, mikä tarkoittaa tosi)|
|PU20,80;|nosta kynä ja siirry kohtaan 20,80|
|LBHello World*;|piirrä tarra|

## Viitteet
 * [Wikipedian HPGL](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL-viiteopas](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

