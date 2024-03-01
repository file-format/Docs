{
  "date": "2021-07-08",
  "keywords": [
"HAR",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"JSON",
"Arkistotiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAR - HTTP-arkistotiedostomuoto",
  "description": "Tiedostomuoto-oppaasi oppiaksesi, mikä on HAR-tiedosto ja API:t, jotka voivat luoda ja avata HAR-tiedoston.",
  "linktitle": "HAR",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ha-fir"
}
},
  "lastmod": "2021-07-08"
}

## Mikä on HAR-tiedosto?

Tiedosto, jossa on .har (HTTP-arkisto) -tiedosto, on HTTP-arkistotiedosto, joka tallentaa istuntotiedot siirrettäväksi useiden selaimien (kuten Chrome, Safari, IE, Firefox jne.) kautta [JSON](/web/json/)-tiedostomuodossa. Internetin kautta palvelimen ja asiakkaan (tässä tapauksessa käyttäjän selaimen) välillä siirrettävä tieto sisältää HTTP-pyyntö- ja vastausotsikot, jotka on tallennettu HAR-tiedostoon. Se sisältää lisäksi yksityiskohtaisia tietoja selaimeen ladattujen verkkosivujen suorituskykytiedoista. HAR-tiedostot voidaan avata missä tahansa tekstieditorissa, kuten Microsoft Windows -käyttöjärjestelmän Notepadissa ja Apple MacOS:n TextEditissä.

## HAR-tiedostomuoto – lisätietoja

HAR-tiedostot tallentavat istuntotiedot pelkkää tekstitiedostoa käyttäen suosittua JSON-muotoa. HAR-tiedostomuodon tekniset tiedot on tuottanut World Web Consortiumin (W3C) Web Performance Group, mutta niitä ei voitu julkaista. Se kuitenkin onnistui määrittämään HTTP-tapahtumien arkistointimuodon.

Pyyntö- ja vastaustietojen siirron valvonnan lisäksi kehittäjät käyttävät HAR-tiedostoja verkkoselaimen suorituskyvyn kirjaamiseen sivun latausnopeuden, sisällön latausajan, ladatun sisällön, selaimen vastauksen saamiseksi suoritettujen kyselyjen ja monien muiden perusteella. .

## Miksi käyttää HAR-tiedostoja?

HAR-tiedostot voivat auttaa parantamaan verkkosivuston suorituskykyä arvioimalla pitkiä latausaikoja, sivun renderöintiaikoja ja vasteaikoja. HAR-tiedostoja voidaan analysoida tällaisten ongelmien löytämiseksi ja verkkosivuston ongelmien ratkaisemiseksi suorituskyvyn parantamiseksi.

## Kuinka luoda HAR-tiedosto?

Joten, kuinka luodaan HAR-tiedosto? No, tämä riippuu siitä, minkä tyyppistä selainta käytät HAR-tiedoston luomiseen. Tässä oppaassa luetellaan Google Chrome -selaimen vaiheet. Menetelmiä HAR-tiedostojen luomiseksi Safarilla, Firefoxilla jne. voidaan helposti etsiä ja seurata Internetistä.

### Vaiheet HAR-tiedoston luomiseen Google Chromella

Seuraavat vaiheet voidaan suorittaa verkkosivulla, jolla on ongelmia.

 1. Avaa Web-sivu Google Chromessa, jossa ongelma tapahtui.
 1. Avaa kehittäjätyökalu (tarkista elementti).
 1. Siirry paneelin vasemmalle puolelle aloittaaksesi tiedoston tallennus. Tässä osassa on pieni pyöreä punainen painike.
 1. Napsauta Tyhjennä-kuvaketta poistaaksesi kaikki selaimessa tallennetut lokitiedot.
 1. Tallentaaksesi haluamasi sisällön yllä olevan kuvan mukaisesti, napsauta hiiren oikeaa painiketta ja napsauta Tallenna HAR-tiedostona

## Viitteet

* [HAR-tiedostomuoto – Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))


