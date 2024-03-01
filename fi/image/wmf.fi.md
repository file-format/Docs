{
  "date": "2019-10-11",
  "keywords": [
"wmf tiedosto",
"wmf tiedostomuoto",
"mikä on wmf-tiedosto",
"tiedosto",
"wmf esimerkki",
"wmf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMF - Microsoft Windowsin metatiedostomuoto",
  "description": "Opi WMF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WMF-tiedostoja.",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on WMF-tiedosto?

WMF-laajennuksella varustetut tiedostot edustavat Microsoft Windows Metafilea (WMF) vektori- ja bittikarttamuotoisten kuvien tallentamiseen. Tarkemmin sanottuna WMF kuuluu grafiikkatiedostomuotojen vektoritiedostomuotoluokkaan, joka on laitteesta riippumaton. Windows Graphical Device Interface (GDI) käyttää WMF-tiedostoon tallennettuja toimintoja kuvan näyttämiseen näytöllä. WMF:n paranneltu versio, joka tunnetaan nimellä Enhanced Meta Files (EMF), julkaistiin myöhemmin, mikä tekee muodosta monipuolisemman. Käytännössä WMF:t ovat samanlaisia kuin SVG.

## WMF-tiedostomuodon tekniset tiedot ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. Tiedostomuoto koostuu sarjasta vaihtelevan pituisia tietueita, jotka sisältävät grafiikan piirustuskomentoja, objektimäärityksiä ja ominaisuuksia. Koska WMF-tiedostot perustuvat GDI:lle annettuihin komentoihin kuvan piirtämistä varten, se tunnetaan myös kuvan digitaalisena tallenteena, jota voidaan toistaa kuvan toistamiseksi. WMF:n täydelliset tiedostomuotomääritykset ovat saatavilla verkossa, ja niitä tulee käyttää WMF-tiedostojen kanssa toimivien sovellusten kehittämisessä. WMF-tiedosto on järjestetty:

* WMF Header Record

* WMF-tietue(t)

* WMF-tiedoston lopputietue


### WMF Header Record ###

**META_HEADER-tietue** sisältää tietoja, jotka määrittelevät metatiedoston ominaisuudet, mukaan lukien:

* Metatiedoston tyyppi

* Metatiedoston versio

* Metatiedoston koko

* Metatiedostossa määritettyjen objektien määrä

* Metatiedoston suurimman yksittäisen tietueen koko


### WMF-sijoitettava otsikkotietue ###

**META_PLACEABLE-tietue** sisältää laajennettua tietoa kuvasta, mukaan lukien:

* Rajaava suorakulmio

* Loogisen yksikön koko, skaalaus

* Tarkistussumma vahvistusta varten


### WMF-ennätys ###

WMF-tietueilla on yleinen muoto, joka on määritelty teknisessä asiakirjassa. Jokainen WMF-tietue sisältää seuraavat tiedot:

* Ennätyskoko

* Tallennustoiminto

* Tallennustoiminnon parametrit, jos niitä on


## Viitteet ##

* [[MS-WMF]: Windowsin metatiedostomuoto](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)


