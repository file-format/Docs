{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"tiedosto",
"laajennus",
"muoto",
"eBook",
"Digitaalinen kirja"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi LRF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LRF-tiedostoja.",
  "title": "LRF-tiedostomuoto - Sonyn kannettava lukijatiedosto",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-fif"
}
},
  "lastmod": "2019-12-12"
}

## Mikä on LRF-tiedosto?

Tiedosto, jonka laajennus on .lrf, on Broad Band eBook (BBeB) -tiedosto, joka sisältää tietoja Sony BBeB:stä, mukaan lukien tekstiä, kuvia ja sivutustietoja. Tiedosto tallennetaan pakatussa binäärimuodossa, joka sisältää otsikon, tietyn määrän objekteja ja objektiindeksin. LRF- ja LRX-tiedostot sisältävät kaksi saatavilla olevaa BBeB-kirjamuotoa. LRF-tiedostoja ei ole salattu, ja ne voidaan kääntää [LRX](/ebook/lrf/)-tiedostoista. LRF-tiedostot voidaan muuntaa useista muista tiedostotyypeistä, mukaan lukien PDF ja HTML. Jos tietokoneesi ei voi avata LRF-tiedostoa, sinulla ei todennäköisesti ole asennettuna ohjelmistoa LRF-tiedostojen avaamiseen tai muokkaamiseen. Ohjelmat, jotka voivat avata LRF-tiedostoja, ovat Caliber, BookDesigner, Makelrf ja Canon Book Creator for Windows, Caliber Linux, Caliber ja Sony Reader for Macintosh.

## Lyhyt historia

LRF-tiedostotyyppi on ennen kaikkea liitetty Line Rideriin, jonka tekijä on [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider on internetin fysiikan lelu, jonka slovenialainen yliopisto-opiskelija Boštjan Čadež keksi syyskuussa 2006. Sonyn eBook eReaders (kuten Sony PRS-500 -lukijat ja Sony Librie) käyttävät LRF-tiedostotunnistetta asiakirjoissaan ja teksteissään. Tämä oma tiedostotyyppi on nyt vanhentunut, samoin kuin siihen liittyvät LRS- ja LRX-tiedostot. Nämä kolme tiedostotyyppiä muodostivat BroadBand eBookin (BBeB), joka lopetettiin vuonna 2010, kun Sony alkoi myydä e-kirjojaan EPUB-muodossa.

## LRF tiedostomuoto

LRF-tiedostomuodon yksityiskohtaiset tiedot ovat saatavilla osoitteessa [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). LRF-tiedosto koostuu:
* otsikko

* useita esineitä

* objektiindeksi.


Kaikki nämä arvot ovat Intelin järjestyksessä (LSB ensin).

### LRF-otsikko

|Siirtymä (heksa) |Koko (tavua) |Nimi/merkitys| Esimerkkiarvo|
---|---|---|---|
|0 |8| LRF Allekirjoitus| 4C 00 52 00 46 00 00 00 = LRF Unicodessa|
|8 |2| versio?| 999 useimmissa tiedostoissa|
|A |2| Psuedo-Encryption |avaintavu 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Objektien lukumäärä |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| tuntematon| 0|
|24 |1| Liput| (16 - takaa eteen, 1 = edestä taakse) 16|
|25 |1| tuntematon |(täyte?) 0|
|26 |2| tuntematon| 1600|
|28 |2| tuntematon| (täyte?) 0|
|2A |2| Korkeus?| 600|
|2C |2| Leveys?| 800|
|2E |1| tuntematon| 24|
|2F |1| tuntematon |(täyte?) 0|
|30 |0x14| tuntematon| nollia|
|44 |4| Vain PlaneStream (0x1E) -objektin objektitunnus| 0x0042|
|48 |4| tuntematon |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Viitteet

* [LRF-tiedostomuoto](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB - Wikipedia](https://en.wikipedia.org/wiki/BBeB)


