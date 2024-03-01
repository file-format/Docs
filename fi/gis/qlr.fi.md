{
  "date": "2019-10-11",
  "keywords": [
"qlr tiedosto",
"qlr tiedostomuoto",
"mikä on qlr-tiedosto",
"tiedosto",
"qlr esimerkki",
"qlr tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QLR - QGIS-kerroksen määritystiedosto",
  "description": "Opi QLR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata QLR-tiedostoja.",
  "linktitle": "QLR",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-ql-fir"
}
},
  "lastmod": "2021-03-14"
}

## Mikä on QLR-tiedosto?

.qlr-tiedosto on Layer Definition -tiedosto, joka sisältää osoittimen kerroksen tietolähteeseen. Tämä on tason [QGIS](https://www.qgis.org/en/site/)-tyylitietojen lisäksi. Tässä tiedostossa on viittaukset kaikkiin aiheeseen liittyviin tyyleihin, ja sitä käytetään yhtenä tietolähteenä, jota käytetään tyylitietojen hankkimiseen. QLR-tiedostoja käyttämällä tietolähteiden tiedot voidaan laittaa tähän yhteen tiedostoon, jota muut sovellukset voivat lukea tyylitietojen lataamiseksi. QLR-tiedostoja voidaan avata millä tahansa tekstieditorilla, kuten Notepad++.

## QLR tiedostomuoto

QLR, samanlainen kuin [QGS](/gis/qgs/), on XML-tiedosto, joka sisältää osoittimia kerrostietolähteeseen XML-tunnisteiden muodossa. Se on samanlainen kuin ArcGIS .lyr-tiedosto. QML-tiedoston ylimmän tason tagit ovat alla olevan kuvan mukaiset.

{{< figure src="../qlr.png" title="" >}}

## Viitteet

* [QGIS](https://www.qgis.org/en/site/)

* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

