{
  "date": "2021-04-08",
  "keywords": [
"lz tiedosto",
"lz tiedostomuoto",
"mikä on lz-tiedosto",
"tiedosto",
"lz esimerkki",
"lz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ - Lzip-pakattu tiedostomuoto",
  "description": "Opi LZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LZ-tiedostoja.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-fiz"
}
},
  "lastmod": "2021-04-19"
}

## Mikä on LZ-tiedosto?

Tiedosto, jonka laajennus on .lz, on pakattu arkistotiedosto, joka on luotu Lzipillä, joka on ilmainen komentorivityökalu pakkausta varten. Se tukee ketjutusta tukitiedostojen pakkaamiseksi. LZ-tiedostot ovat mediatyyppisiä application/lzip-tiedostoja ja ne tukevat korkeampia pakkaussuhteita kuin [BZ2](/compression/bz2/). LZ perustuvat LZMA-algoritmiin (Lempel-Ziv-Markov-ketju) ja sisältävät 32-bittisen CRC-tarkistussumman ja tunnistetavuja tiedoston eheyden tarkistamiseksi.

## LZMA pakattu muoto

LZMA-pakattu muoto koostuu pakatusta bittivirrasta, joka on koodattu adaptiivisella binäärialuekooderilla. Virta on jaettu paketeiksi. Jokainen paketti kuvaa joko yhden tavun tai LZ77-sekvenssin. Kunkin paketin pituus ja etäisyys on koodattu implisiittisesti tai eksplisiittisesti.

Seitsemän pakettityyppiä ovat seuraavat ({{HYPERLINKKI}})

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + tavukoodi| LIT| Yksi tavu koodattu käyttämällä adaptiivista binäärialuekooderia.|
|1+0 + len + dist| OTTELU| Tyypillinen LZ77-sekvenssi, joka kuvaa sekvenssin pituutta ja etäisyyttä.|
|1+1+0+0| SHORTREP| Yksitavuinen LZ77-sekvenssi. Etäisyys on yhtä suuri kuin viimeksi käytetty LZ77-etäisyys.|
|1+1+0+1 + len| LONGREP[0]| LZ77-sarja. Etäisyys on yhtä suuri kuin viimeksi käytetty LZ77-etäisyys.|
|1+1+1+0 + len| LONGREP[1]| LZ77-sarja. Etäisyys on yhtä suuri kuin toiseksi viimeksi käytetty LZ77-etäisyys.|
|1+1+1+1+0 + len| LONGREP[2]| LZ77-sarja. Etäisyys on yhtä suuri kuin kolmanneksi viimeksi käytetty LZ77-etäisyys.|
|1+1+1+1+1 + len| LONGREP[3]| LZ77-sarja. Etäisyys on sama kuin neljänneksi viimeksi käytetty LZ77-etäisyys.|


## Viitteet

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)

* [Lzip](https://en.wikipedia.org/wiki/Lzip)


