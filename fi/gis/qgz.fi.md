{
  "date": "2021-03-18",
  "keywords": [
"qgz tiedosto",
"qgz tiedostomuoto",
"mikä on qgz-tiedosto",
"tiedosto",
"qgz esimerkki",
"qgz tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "QGZ - Quantum GIS Compressed Project",
  "description": "Opi QGZ-tiedostomuodosta, joka on vain pakattu QGS, ja API:ista, jotka voivat luoda ja avata QGZ-tiedostoja.",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-fiz"
}
},
  "lastmod": "2021-03-18"
}

## Mikä on QGZ-tiedosto?

**QGZ**-tiedostomuoto on pakattu arkisto, joka sisältää [QGS](/gis/qgs/)-tiedoston ja QGD-tiedoston. QGD-tiedosto on qgis-projektin sqlite-tietokanta, joka koostuu projektin aputiedoista. Jos aputietoja ei ole, QGD-tiedosto jää tyhjäksi.

## Lisätietoja QGZ-tiedostomuodosta

QGZ esiteltiin uutena muunnelmana **QGIS 3 -projektitiedostomuodosta**. Tämä muoto on pakattu säilö QGS xml -tiedostolle. Jos käyttäjät valitsevat QGD:n, joka on valinnainen muoto, tässä tapauksessa kontti on hyödyllinen lisätallennustietokannan tallentamiseen.

Klassisessa tilassa aputietokanta tallennetaan xml-tiedoston mukana tiedostona, jonka pääte on .qgd. Pakattua säilöä valittaessa .qgd-tiedosto sisällytetään .qgz-tiedostoon. Se vain helpottaa käyttäjiä ilman ongelmia, käyttäjät eivät voi poistaa sitä tai unohtaa kopioida sitä jakaessaan projektitiedostoja!


## Viitteet

* [QGZ – uusi oletusprojektitiedostomuoto QGIS:lle](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

