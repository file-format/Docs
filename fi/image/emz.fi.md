{
  "date": "2019-10-11",
  "keywords": [
"emz tiedosto",
"emz tiedostomuoto",
"mikä on emz-tiedosto",
"tiedosto",
"emz esimerkki",
"emz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMZ-tiedostomuoto - Windowsin pakattu Enhanced Meta -tiedosto",
  "description": "Opi EMZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EMZ-tiedostoja.",
  "linktitle": "EMZ",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-fiz"
}
},
  "lastmod": "2020-10-24"
}

## Mikä on EMZ-tiedosto?

Tiedosto, jonka pääte on .emz, on Enhanced Metafile -tiedosto ([EMF](/image/emf/)-tiedosto) pakattu säilö. Nämä pakataan käyttämällä [GZIP](/compression/gz/)-pakkaustekniikkaa, joka on yleisesti käytetty pakkausmenetelmä UNIX- ja LINUX-käyttöjärjestelmissä. Pura ZIP (/compression/zip/), GZIP pakkaa arkiston kokonaisuutena yksittäisten tiedostojen pakkaamisen sijaan. EMZ-tiedostot ovat kooltaan pienempiä kuin EMF-tiedostot ja auttavat nopeassa siirrossa online-tiedostojen jakamisen aikana. Joitakin sovelluksia, jotka voivat avata EMZ-tiedostoja, ovat Microsoft Visio 2019, Microsoft Office 2019, XnView MP ja File Viewer Plus.

## EMZ tiedostomuoto

EMZ-tiedostot ovat [Gzip](/compression/gz/) pakattuja ja sisältävät [EMF](/image/emf/). Gzip käyttää DEFLATE-algoritmia arkiston pakkaamiseen ja on erilainen pakkaamisessa. EMZ-tiedosto voidaan purkaa käyttämällä GZip-pakkausapuohjelmia, kuten GNU Zip. Tiedostomuoto koostuu:

 * Tiedoston otsikko
 * Valinnaiset otsikot
 * Pakatut tiedot
 * Tiedoston alatunniste

Internet Engineering Task Forcen (IETF) julkaisema GZIP-tiedostomuoto [specifications version 4.3](https://datatracker.ietf.org/doc/html/rfc1952) sisältää yksityiskohtaisia tietoja tiedostomuodosta.

## Viitteet

 * [RFC1952: GZIP-tiedostomuodon määrittely](https://datatracker.ietf.org/doc/html/rfc1952), tekijä [IETF](https://www.ietf.org/)
 * [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

