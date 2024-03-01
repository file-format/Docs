{
  "date": "2021-04-08",
  "keywords": [
"rpm tiedosto",
"rpm tiedostomuoto",
"mikä on rpm-tiedosto",
"tiedosto",
"rpm esimerkki",
"rpm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RPM - Red Hat Package Manager -tiedosto",
  "description": "Opi RPM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RPM-tiedostoja.",
  "linktitle": "RPM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rp-fim"
}
},
  "lastmod": "2021-04-09"
}

## Mikä on RPM-tiedosto?

Tiedosto, jonka laajennus on .rpm, on Red Hat Linux -käyttöjärjestelmäpaketti ohjelmien asentamiseen Linux-järjestelmiin. Red Hat Package Manager käyttää RPM-tiedostomuotoa ja on ilmainen ja avoimen lähdekoodin paketinhallintajärjestelmä. Vaikka RPM-tiedostoja voidaan käyttää sellaisenaan ohjelmien asentamiseen, ne voidaan muuntaa muihin pakettimuotoihin, kuten [DEB](/compression/deb/) käyttämällä Debian-ohjelmaa nimeltä Alien.

## RPM-tiedostomuoto

RPM-tiedosto on binaaritiedosto, joka voi sisältää joukon tiedostoja. Useimmiten RPM-tiedostot ovat binäärisiä RPM:itä, jotka ovat ohjelmiston käännettyjä suoritettavia tiedostoja. RPM-tiedosto voi sisältää lähde-RPM:itä (SRPM), joita voidaan käyttää paketin rakentamiseen lähdekoodista. RPM-tiedostomuoto koostuu neljästä osasta.

 * Lead - Se tunnistaa tiedoston RPM-tiedostoksi
 * Allekirjoitus - Sitä voidaan käyttää eheyden ja/tai aitouden varmistamiseksi
 * Otsikko – Sisältää metatiedot, mukaan lukien paketin nimen, version, arkkitehtuurin, tiedostoluettelon jne.
 * Tiedostoarkisto – Tunnetaan myös nimellä hyötykuorma, joka on yleensä cpio-muodossa, pakattuna [GZIP]:llä (/compression/gz/)

## Viitteet

* [RPM - Wikipedia](https://rpm.org)

* [RPM-dokumentaatio](https://rpm.org/documentation.html)


