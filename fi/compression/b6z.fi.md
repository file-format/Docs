{
  "date": "2019-10-11",
  "keywords": [
"b6z tiedosto",
"b6z tiedostomuoto",
"mikä on b6z-tiedosto",
"tiedosto",
"b6z esimerkki",
"b6z tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "B6Z - B6ZIP-arkistotiedostomuoto",
  "description": "Opi B6Z-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata B6Z-tiedostoja.",
  "linktitle": "B6Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-b6-fiz"
}
},
  "lastmod": "2021-04-05"
}

## Mikä on B6Z-tiedosto?

Tiedosto, jonka laajennus on .b6z, on pakattu arkistotiedosto, joka on luotu macOS-ohjelmistosovellus [B6Zip](http://b6zip.com), jota käytetään tiedostojen pakkaamiseen ja purkamiseen. Se on suhteellisen uusi arkistomuoto, joka mahdollistaa suuremman pakkaussuhteen. B6Z:llä on avoin arkkitehtuuri ja se tukee tiedostokokoja 900 000 PB asti. Se tukee tietojen pakkaamista, virheiden palautusta ja tiedostojen kattavuutta. B6Zip-apuohjelma on saatavilla ilmaiseksi MacOS:lle erityyppisten pakattujen tiedostojen avaamiseen, mukaan lukien B6Z.

## B6Z tiedostomuoto

B6Z-tiedostomuoto perustuu avoimeen arkkitehtuuriin ja tarjoaa vankan pakkauksen AES-256-salausalgoritmilla. Se käyttää LZMA2:ta oletuspakkausmenetelmänä, mutta tukee myös muita pakkausmenetelmiä seuraavasti.

|Menetelmä|Kuvaus|
---|---|
|LZMA |LZ77-algoritmin optimoitu versio|
|LZMA2| LZMA|:n parannettu versio
|Tyhjennä| Tavallinen LZ77-algoritmi|
|BZip2| Vakio BWT-algoritmi|
|PPMD| Dmitry Shkarinin PPMdH|

B6Zip-apuohjelma tukee kaikkia näitä pakkausstandardeja ja on erittäin optimoitu, mikä johtaa suureen nopeuteen. Se tukee tiedostomuotojen [ZIP](/compression/zip/), [TAR](/compression/tar/) ja [RAR](/compression/rar/) käyttöä. B6Z-tiedostoissa on MIME-tyyppinen application/x-b6z-pakattu.

## Viitteet

* [B6Zip](http://b6zip.com)


