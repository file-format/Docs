{
  "date": "2021-04-08",
  "keywords": [
"lzma tiedosto",
"lzma tiedostomuoto",
"mikä on lzma-tiedosto",
"tiedosto",
"lzma esimerkki",
"lzma tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA pakattu tiedostomuoto",
  "description": "Mikä on LZMA-tiedosto ja API:t, jotka voivat luoda ja avata LZMA-tiedostoja.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-fia"
}
},
  "lastmod": "2021-04-18"
}

## Mikä on LZMA-tiedosto?

Tiedosto, jonka pääte on .lzma, on pakattu arkistotiedosto, joka on luotu LZMA-pakkausmenetelmällä (Lempel-Ziv-Markov chain Algorithm). Näitä löytyy/käytetään pääasiassa Unix-käyttöjärjestelmässä ja ne ovat samanlaisia kuin muut pakkausalgoritmit, kuten [ZIP](/compression/zip/) tiedostokoon minimoimiseksi. LZMA on vanha tiedostomuoto, joka ollaan tai on korvattu .xz-muodolla. .lzma-muodon MIME-tyyppi on \`application/x-lzma'. Tämän tiedostomuodon on suunnitellut Igor Pavlov käytettäväksi LZMA SDK:ssa.

## LZMA tiedostomuoto

LZMA-tiedosto koostuu kahdesta pääosasta:

 1. Otsikko
 1. Pakatut tiedot


### LZMA-otsikko

LZMA-tiedostoilla on 13-tavuinen otsikko, jota seuraa LZMA-pakatut tiedot. LZMA-otsikko koostuu:

 * Ominaisuudet
 * Sanakirjan koko
 * Pakkaamaton koko

#### LZMA-otsikon ominaisuudet

Ominaisuudet-kenttä sisältää kolme ominaisuutta. Suluissa on lyhenne, jota seuraa ominaisuuden arvoalue. Kenttä koostuu

1) kirjaimellisten kontekstibittien lukumäärä (lc, [0, 8]);
2) kirjaimellisten sijaintibittien lukumäärä (lp, [0, 4]); ja
3) paikkabittien lukumäärä (pb, [0, 4]).

#### LZMA-sanakirjan koko

Tämä tallennetaan etumerkittömänä 32-bittisenä pienenä kokonaislukuna, jonka arvot vaihtelevat välillä 2^n ja 2^n + 2^(n-1). LZMA Utils voi purkaa tiedostoja minkä tahansa sanakirjakoon kanssa.

#### Pakkaamaton koko
Pakkaamaton koko tallennetaan etumerkittömänä 64-bittisenä pienenä kokonaislukuna. Erikoisarvo 0xFFFF_FFFF_FFFF_FFFF osoittaa, että pakkaamaton koko on tuntematon. Arvoa edustaa hyötykuorman loppumerkki (\*), jos ja vain jos pakkaamaton koko on tuntematon.

## Viitteet

* [Lempel–Ziv–Markov-ketjualgoritmi](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
