{
  "date": "2019-10-11",
  "keywords": [
"tbz tiedosto",
"tbz tiedostomuoto",
"mikä on tbz-tiedosto",
"tiedosto",
"tbz esimerkki",
"tbz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TBZ - Bzip-pakattu terva-arkisto",
  "description": "Opi TBZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TBZ-tiedostoja.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tb-fiz"
}
},
  "lastmod": "2021-04-05"
}

## Mikä on TBZ-tiedosto?

Tiedosto, jonka laajennus on .tbz, on pakattu arkisto, joka käyttää BZIP-pakkausta sisältötiedostojen koon pienentämiseen. TBZ-tiedostot ovat itse asiassa UNIX [TAR](/compression/tar/) -arkistoituja tiedostoja, jotka pakataan BZIP:llä. Viimeisin toisen tason pakkaus on [BZIP2](/compression/bz2/), joka korvasi BZIP:n. TBZ-tiedostomuoto sopii suurten tiedostojen siirtämiseen. TBZ-tiedostoja voidaan avata/purkaa ohjelmilla, kuten 7-Zip, PeaZip ja jZip. Linux- ja macOS-käyttäjät voivat myös avata TBZ:n BZIP2-komennolla pääteikkunasta.

## TBZ tiedostomuoto

TBZ-tiedostot ovat itse asiassa pakattuja arkistoja, jotka on luotu BZIP/[BZIP2](/compression/bz2/)-pakkauksella. Tälle tiedostomuodolle ei ole saatavilla virallisia määrityksiä. Epävirallinen [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) osoittaa kuitenkin, että .bz2-virta koostuu 4-tavuisesta otsikosta, jota seuraa nolla tai useampia pakattuja lohkoja.

## Viitteet ##

* [BZIP2-muodon tekniset tiedot](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


