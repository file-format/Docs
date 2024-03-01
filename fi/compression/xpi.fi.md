{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XPI - monikäyttöinen asennuspakettitiedosto",
  "description":"Opi XPI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XPI-tiedostoja.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Mikä on XPI-tiedosto?

XPI-tiedosto on asennusarkisto, joka on pakattu tiedoston koon pienentämiseksi. Mozilla-sovellukset käyttävät sitä lisäosien ja lisäosien asentamiseen. Se sisältää asennuskomentosarjan tai luettelon tiedoston juuressa sekä useita datatiedostoja. XPI-tiedosto voi sisältää teemoja, työkalupakkia tai Firefox-laajennuksia, jotka käyttäjä voi asentaa osaksi Firefox-selainta, Thunderbirdiä tai SeaMonkeya.

## XPI-tiedostomuoto - lisätietoja

XPI-tiedostot tallennetaan levylle [ZIP](/compression/zip/)-arkistojen muodossa, jotka yhdistävät useita tiedostoja yhdeksi pakatuksi tiedostoksi. XPI-tiedoston sisällä olevat tiedostot voivat sisältää asennusskriptitiedostoja, kuten JS, ja verkkotiedostoja, kuten [CSS](/web/css/), [HTML](/web/html/) ja [JSON](/web/json/). Joskus se voi sisältää myös [PNG](/image/png/) kuvatiedostoa, joita lisäosat voivat käyttää kuvakkeina.

### Kuinka tarkastella XPI-tiedoston sisältöä?

XPI-tiedosto on käytännössä ZIP-arkisto, jonka sisältöä voi tarkastella seuraavien vaiheiden avulla.

 * Muuta tiedoston tunniste XPI:stä ZIP:ksi
 * Pura tiedoston sisältö millä tahansa tavallisella purkuohjelmalla, kuten WinZip (Windows, Mac), 7-Zip (Windows) tai Apple Archive Utility (Mac).

### Asenna XPI-tiedosto Firefox Androidiin

Useimmiten ihmiset ovat uteliaita tietämään, voidaanko XPI-tiedostoja asentaa Firefoxiin Android-laitteille. Androidissa voit asentaa lisäosan XPI-tiedostosta etsimällä tiedoston ja avaamalla sen Firefoxilla.

## Viitteet

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)

* [Kuinka voin avata XPI-tiedostolaajennuksen?](https://support.mozilla.org/en-US/questions/1009049)


