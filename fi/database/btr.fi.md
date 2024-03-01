{
  "date": "2021-09-06",
  "keywords": [
"btr",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Btrieve-tietokanta"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi BTR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BTR-tiedostoja.",
  "title": "BTR - Btrieve-tietokantatiedosto",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bt-fir"
}
},
  "lastmod": "2021-09-06"
}

## Mikä on BTR-tiedosto?

Tiedosto, jonka pääte on .btr, on tietokantatiedosto, jonka on luonut [Btrieve](https://www.actian.com/) tapahtumatietokantasovellus. Toisin kuin relaatiotietokannan hallintajärjestelmät (RBMS), Btrieve perustuu Indexed Sequential Access Method (ISAM) -menetelmään, joka on tapa tallentaa tietoja nopeaa hakua varten. BTR-tiedosto tallentaa kokoelman tietueita, ja sitä käytetään raporttien luomiseen vaatimusten mukaisesti. BTR-tiedostoja voidaan avata käyttämällä Pervasive Btrieve Database Manageria, Pervasive PSQL Maintenance Utilityä ja Legend Software BTRIEVE Vieweria.

## BTR-tiedostorakenne – lisätietoja

Sisäinen tietorakenne ja kunkin tavun kohdistus BTR-tiedoston rakenteessa ei ole julkisesti saatavilla. Kuitenkin Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * GNU C/C++
 * Micro Focus COBOL
 * Microsoft Visual Basic
 * Microsoft Visual C++
 * Watcom C/C++

Tietojen hakeminen BTR-tiedostosta riippuu siihen liittyvästä DDF-tiedostosta. Ilman DDF-tiedostoa tietojen hakeminen tällaisesta tiedostosta ei ole helppoa.

## Viitteet

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

