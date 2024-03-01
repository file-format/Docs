{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Sivun asettelu",
"Kapseloitu PostScript"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi EPS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EPS-tiedostoja.",
  "title": "EPS-tiedostomuoto - Kapseloitu PostScript-tiedosto",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on EPS-tiedosto?

.eps-tiedosto on kuvatiedosto, joka tallennetaan levylle Encapsulated Postscript -tiedostomuodossa. Se voi sisältää minkä tahansa tekstin, grafiikan ja kuvien yhdistelmän. EPS-tiedostot voivat sisältää myös bittikartan esikatselukuvan, joka on kapseloitu sisälle, jotta ne voivat näyttää sovelluksia, jotka voivat avata tällaisia tiedostoja.

## EPS-tiedostomuodon lyhyt historia

Nopea katsaus EPS-tiedostomuotoon historian näkökulmasta paljastaa seuraavat tiedot:

* Adobe julkaisi EPS:n ensimmäisen version joskus 1985-1988

* EPS-spesifikaation versio 2.0 julkaistiin tammikuussa 1989

* EPS:n version 3.0 spesifikaatio julkaistiin erillisenä asiakirjana vuonna 1992; tämä on viimeisin julkaistu versio.


EPS yhdessä Adoben PostScript Language Document Structuring Conventions -määrityksen kohdassa 9 kuvatun Open Structuring Conventions -laajennusmekanismin kanssa muodosti perustan Adobe Illustrator Artwork -tiedostomuodon varhaisille versioille.

## EPS-tiedostomuoto

EPS on patentoitu mutta julkisesti dokumentoitu muoto, ja EPS-tiedostomuotomääritykset ovat saatavilla julkisesti kehittäjien viitteeksi. EPS on [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) -yhteensopiva tiedostomuoto ja noudattaa kaikkia DSC:n asettamia sääntöjä. DSC on Adoben PostScript-asiakirjojen erityinen tiedostomuoto. Kaikkien sovellusten, jotka väittävät pystyvänsä lukemaan EPS-tiedostoja, tulee olla DSC-yhteensopivia.

EPS-tiedosto koostuu kahdesta pääosasta, kuten alla selitetään.

### Esikatselukuva ###

Tyypillinen EPS-tiedosto sisältää esikatselukuvan muodossa, joka on tarkoitettu kätevästi käytettäväksi työnkulussa, joka sisältää useita järjestelmiä tai sovelluksia. Esikatselun tarkoituksena on saada kuva sellaisessa muodossa, jonka useimmat grafiikkasovellukset voivat hahmontaa. esikatselu on yleensä pienempi resoluutio, pikselimitat ja/tai bittisyvyys. Esikatselutiedosto voi olla jossakin useista muodoista. EPS_3:n määrittelyssä on kolme laitekohtaista esikatselumuotoa:

* Apple Macintoshissa QuickDraw-sovelluksen käyttämä PICT-kuva

* DOS-tietokoneissa TIFF-bittikartta

* Windowsin metatiedosto.


PICT ja Windows Metafile voivat sisältää sekä bittikarttatietoja että vektorigrafiikkaa. Lisäksi spesifikaatio määrittelee erittäin yksinkertaisen laitteesta riippumattoman esityksen upotetulle bittikartta-esikatselukuvalle. Tämä esitys tunnetaan nimellä Encapsulated PostScript Interchange Format (EPSI).

EPSI-esikatselu on ASCII-heksadesimaalimuotoinen bittikartta, joka on kääritty muutaman PostScript-kommentin väliin tunnistamista varten ja joka on tarkoitettu yksinkertaiseksi ja helposti siirrettäväksi. Eri esikatselumuotojen EPS-tiedostojen erottamiseksi EPS-spesifikaatioissa suositeltiin erilaisia DOS-tiedostotunnisteita ja Macintosh-tiedostotyyppejä.

### PostScript-koodi

EPS-tiedostomuodon tulee sisältää vähintään seuraavat tiedot:

* otsikkokommentti, %!PS-Adobe-3.0 EPSF-3.0

* ja rajoituslaatikon kommentti %%BoundingBox: llx lly urx ury, joka kuvaa kuvan rajoja. Nämä neljä argumenttia vastaavat rajauslaatikon vasenta alakulmaa (llx, lly) ja oikeaa yläkulmaa (urx, ury).


EPS-tiedosto ei voi käyttää seuraavia operaattoreita:

* bändilaite,

* Cleardictstack

* kopioi sivu

*poistosivu

* poistumispalvelin

*kehyslaite

* grestoreall

* initclip

* aloitusgrafiikka

* initmatriisi

* lopeta

* renderöintikaistat

* aseta globaali

* aseta sivulaite

* setshared

* aloita työ.


## EPS:n muuntaminen muihin tiedostomuotoihin

EPS-tiedostot voidaan muuntaa vakiokuvamuotoihin, kuten [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) ja [PDF](/pdf/) käyttämällä erilaisia sovelluksia, kuten Adobe Illustrator, Photoshop ja PaintShop Pro.

Koska EPS-tiedostoissa on {{HYPERLINKKI}}, Office 2016, Office 2013, Office 2010 ja Office 365 ovat poistaneet käytöstä mahdollisuuden lisätä EPS-tiedostoja Office-asiakirjoihin.

## Viitteet

* [Encapsulated PostScript - Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


