{
  "date": "2019-12-09",
  "keywords": [
"zl tiedosto",
"zl tiedostomuoto",
"mikä on zl-tiedosto",
"tiedosto",
"zl esimerkki",
"zl tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL - ZLIP pakattu tiedostomuoto",
  "description": "Opi ZL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ZL-tiedostoja.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-fil"
}
},
  "lastmod": "2021-04-14"
}

## Mikä on ZL-tiedosto?

Tiedosto, jonka laajennus on .zl, on ZLIP-pakattu tiedostomuoto, joka käyttää DEFLATE-pakkausalgoritmin muunnelmaa tiedostojen pakkaamiseen. Se on riippumaton suorittimen tyypistä, käyttöjärjestelmästä, tiedostojärjestelmästä ja merkistöstä, ja siksi sitä voidaan käyttää tietojen vaihtoon. ZLIP-pakkauksen tekniset tiedot ovat saatavilla osoitteessa [IETF site](https://tools.ietf.org/html/rfc1950), ja niihin voi viitata kehittäjän näkökulmasta.

## ZL tiedostomuoto

Zlib-virralla on seuraava rakenne:

 * CMF (Compression Method and flags) - Tämä tavu on jaettu 4-bittiseen pakkausmenetelmään ja 4-bittiseen tietokenttään pakkausmenetelmästä riippuen.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * CM (Compression method) - Se tunnistaa tiedostossa käytetyn pakkausmenetelmän. Sen arvot ja vastaava pakkausmenetelmä ovat seuraavat.

| CM-arvo| Kompressio|
|---|---|
|CM = 8|DEFLATE ikkunan koolla enintään 32K|
|CM = 15|Varattu|

 * `CINFO (pakkaustiedot)` - Jos CM = 8, CINFO on LZ77-ikkunan koon perus-2 logaritmi miinus kahdeksan (CINFO=7 tarkoittaa 32 kt:n ikkunan kokoa).

 * FLG (FLaGs) - Tämä lipputavu on jaettu seuraavasti:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Viitteet ##

* [Zlib-tiedostomuodon tekniset tiedot](https://tools.ietf.org/html/rfc1950)


