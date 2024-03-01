{
  "date": "2021-04-22",
  "keywords": [
"aps tiedosto",
"visual studio aps-tiedosto",
"laajennus",
"muoto",
"aps tiedosto visual studio",
"aps tiedostopääte",
"kuinka avata aps-tiedosto",
"APS tiedostomuoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "APS - Visual C++ -resurssitiedosto",
  "description": "Opi APS-tiedostomuodosta APS-esimerkillä ja API-liittymillä, jotka voivat luoda ja avata APS-tiedostoja.",
  "linktitle": "APS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ap-fis"
}
},
  "lastmod": "2021-04-22"
}

## Mikä on APS-tiedostomuoto?
APS-tiedoston luo Visual C++, Microsoftin ohjelmistokehityssovellus. Se säästää projektiin sisällytetyn resurssin binääriesityksen ja mahdollistaa sovelluksen lataamisen resursseja nopeammin. Löydät helposti nämä tiedostot .aps-tiedostotunnisteella. Itse asiassa resurssien editorit eivät lue suoraan resource.h-tiedostoja, minkä vuoksi resurssien kääntäjä kokoaa ne .aps-tiedostoiksi, jotka resurssieditorit käyttävät.

## APS tiedostomuoto
APS-tiedostomuoto on vain käännösvaihe ja tallentaa vain symbolisia tietoja. Ei-symboliset tiedot, kuten kommentointi, hylätään käännösprosessin aikana. Kun esimerkiksi tallennat, resurssien muokkausohjelma korvaa resurssin komentosarjatiedoston ja resource.h-tiedoston. Kaikki muutokset itse resursseihin pysyvät sisällytettyinä resurssin komentosarjatiedostoon, mutta kommentit menetetään aina, kun resurssin komentosarjatiedosto korvataan.


## Viitteet

 * [Resurssitiedostot (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 

