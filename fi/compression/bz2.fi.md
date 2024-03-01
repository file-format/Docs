{
  "date": "2019-10-11",
  "keywords": [
"bz2 tiedosto",
"bz2 tiedostomuoto",
"mikä on bz2-tiedosto",
"tiedosto",
"bz2 esimerkki",
"bz2 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 - Pakattu tiedostomuoto",
  "description": "Opi tuntemaan, mikä on BZ2-tiedosto ja API:t, jotka voivat luoda ja avata BZ2-tiedostoja.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-fi2"
}
},
  "lastmod": "2020-09-05"
}

## Mikä on BZ2-tiedosto?

BZ2 ovat pakattuja tiedostoja, jotka on luotu käyttämällä [BZIP2](http://www.bzip.org/) avoimen lähdekoodin pakkausmenetelmää, useimmiten UNIX- tai Linux-järjestelmässä. Sitä käytetään yhden tiedoston pakkaamiseen, eikä sitä ole tarkoitettu useiden tiedostojen arkistointiin. Tämä on toisin kuin samojen alustojen TAR-tiedostomuoto, joka arkistoi useita tiedostoja yhdeksi tiedostoksi ilman pakkausta. BZ2-muodossa pakatut tiedostot voidaan purkaa sovelluksilla, kuten [WinZip](https://www.winzip.com/win/en/). BZIP2 käyttää Run-Length Encoding (RLE)- tai [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform)-pakkausalgoritmia korkean pakkaustason saavuttamiseksi.

## BZ2 tiedostomuoto

Tälle tiedostomuodolle ei ole saatavilla virallisia määrityksiä. Kuitenkin epävirallinen [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) osoittaa, että .bz2-virta koostuu 4-tavuisesta otsikosta, jota seuraa nolla tai useampia pakattuja lohkoja. Sitä seuraa välittömästi virran loppumerkki, joka sisältää 32-bittisen CRC:n koko käsitellylle tekstivirralle. Pakattujen lohkojen välillä ei ole pehmustetta ja kaikki lohkot on kohdistettu bittikohtaisesti.

## Pura/pura BZ2-tiedosto

Voit purkaa BZ2-tiedoston Windows- ja Mac OS -käyttöjärjestelmissä käyttämällä ohjelmistoa, kuten WinZip. Linuxissa seuraava komento terminaalissa.

```
bzip2 -d filename.bz2
```

## Viitteet

* [BZIP2-muodon tekniset tiedot](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


