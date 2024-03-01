{
  "date": "2019-10-11",
  "keywords": [
"wmz tiedosto",
"wmz tiedostomuoto",
"mikä on wmz-tiedosto",
"tiedosto",
"wmz esimerkki",
"wmz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMZ-tiedostomuoto - Pakattu Windowsin metatiedosto",
  "description": "Opi WMZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WMZ-tiedostoja.",
  "linktitle": "WMZ",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-fiz"
}
},
  "lastmod": "2020-10-24"
}

## Mikä on WMZ-tiedosto?

Tiedosto, jonka pääte on .wmz, on {{HYPERLINKKI}}:n pakattu versio, ja sitä käytetään metatiedostojen tallentamiseen. Se on Microsoft Office -sovellusten vanhempien versioiden luoma keskitason tiedosto, jota ei käytetä kovinkaan yleisesti. WMZ-tiedostot luodaan tallennettaessa asiakirjoja [HTML](/web/html/)-muotoon. Näitä voidaan luoda myös lähetettäessä sähköpostidokumentteja, jotka sisältävät upotettuja leikekuvia, yhtälöitä jne. WMZ-tiedostoja avattavia sovelluksia ovat (mutta ei rajoittuen) Corel Winzip ja Apple Archive Utility.

## WMZ tiedostomuoto

WMZ-tiedostot ovat [Gzip](/compression/gz/) pakattuja ja sisältävät [WMF](/image/wmf/). Gzip käyttää DEFLATE-algoritmia arkiston pakkaamiseen. GZIP eroaa [ZIP](/compression/zip/)-arkistomuodosta, koska se käyttää pakkausalgoritmia täydelliseen arkistointiin yksittäisten tiedostojen sijaan. Tiedostomuoto koostuu:

 * Tiedoston otsikko
 * Valinnaiset otsikot
 * Pakatut tiedot
 * Tiedoston alatunniste

Internet Engineering Task Forcen (IETF) julkaisema GZIP-tiedostomuoto [specifications version 4.3](https://datatracker.ietf.org/doc/html/rfc1952) sisältää yksityiskohtaisia tietoja tiedostomuodosta.

## Viitteet

 * [RFC1952: GZIP-tiedostomuodon määrittely](https://datatracker.ietf.org/doc/html/rfc1952), tekijä [IETF](https://www.ietf.org)
 * [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

