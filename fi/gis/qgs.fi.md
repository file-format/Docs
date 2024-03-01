{
  "date": "2019-10-11",
  "keywords": [
"qgs tiedosto",
"qgs tiedostomuoto",
"mikä on qgs-tiedosto",
"tiedosto",
"qgs esimerkki",
"qgs tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QGS - QGIS-projektitiedostomuoto",
  "description": "Opi QGS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata QGS-tiedostoja.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on QGS-tiedosto?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS-tiedostomuoto

QGS-tiedostot ovat [XML](/web/xml/)-muodossa ja tallentavat projektitiedot XML-tunnisteina. QGS-tiedosto sisältää tietoja, kuten:

 * projektin nimi
 * projekti CRS
 * kerrospuu
 * napsautusasetukset
 * suhteet
 * karttakankaan laajuus
 * projektimallit
 * legenda
 * karttanäkymän telakat (2D ja 3D)
 * tasot, joissa on linkit taustalla oleviin tietojoukkoihin (tietolähteisiin) ja muihin tasoominaisuuksiin, mukaan lukien laajuus, SRS, liitokset, tyylit, renderöijä, sekoitustila, läpinäkyvyys ja paljon muuta.
 * projektin ominaisuudet

### QGS huipputason XML-tunnisteet

{{< figure src="../qgstoplevel.png" title="" >}}

### Laajennetut huipputason projektikerroksen tunnisteet

{{< figure src="../qgstoplevel.png" title="" >}}

## Viitteet

* [QGIS](https://www.qgis.org/en/site/)


