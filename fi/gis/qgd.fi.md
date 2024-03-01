{
  "date": "2021-03-18",
  "author": {
    "display_name": "Muhammad Umar",
    "keywords": [
"QGD",
"QGIS-projektin Sqlite-tietokanta",
"laajennus",
"muoto",
"QGIS",
"Aputietokanta",
"Mikä on QGD-tiedosto"
]
},
  "draft": "false",
  "toc": true,
  "title": "QGD - QGIS-projektin Sqlite-tietokanta",
  "description": "Opi QGD:stä, joka on QGIS-projektin sqlite-tietokanta, ja API:ista, jotka voivat luoda ja avata QGD-tiedostoja.",
  "linktitle": "QGD",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-fid"
}
},
  "lastmod": "2021-03-18"
}

## Mikä on QGD-tiedosto?

Tiedosto, jonka tunniste on .QGD-tiedosto, on itse asiassa **QGIS**-projektin sqlite-tietokanta, joka sisältää projektin aputiedot. QGD-tiedosto jää tyhjäksi, jos projektille ei ole lisätietoa.

## Lisätietoja QGD-tiedostomuodosta

Klassisessa tilassa aputietokanta tallennetaan xml-tiedoston mukana tiedostona, jonka pääte on .qgd. **Auxiliary Database** -järjestelmä mahdollistaa tietojen lukemisen ja kirjoittamisen järjestelmään vaihtoehtoisena tapana. Kun luot QGZ:tä, joka on pakattu säilö, .qgd-tiedosto sisällytetään .qgz-tiedostoon.

## Mikä on aputietokanta?
Aputietokanta on itse asiassa valmiustilassa oleva tietokantajärjestelmä, joka luodaan vastauksena kohdetietokannan päällekkäisyyteen. Aputietokanta on itse asiassa kaksoistietokanta, joka olisi tietokanta, johon kopioit. Jos esimerkiksi määrität valmiustilatietokannan käyttämällä kaksoistietokantaa, lähdetietokanta on kohde ja valmiustilatietokanta tunnetaan aputietokannana.


## Viitteet

* [QGZ – uusi oletusprojektitiedostomuoto QGIS:lle](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

