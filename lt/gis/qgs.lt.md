{
  "date": "2019-10-11",
  "keywords": [
"qgs failą",
"qgs failo formatas",
"kas yra qgs failas",
"failą",
"qgs pavyzdys",
"qgs failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QGS – QGIS projekto failo formatas",
  "description": "Sužinokite apie QGS failo formatą ir API, kurios gali kurti ir atidaryti QGS failus.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra QGS failas?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS failo formatas

QGS failai yra [XML](/web/xml/) formato ir saugo projektų duomenis kaip XML žymas. QGS faile yra tokios informacijos kaip:

 * projekto pavadinimas
 * projektas CRS
 * sluoksnio medis
 * fiksavimo nustatymai
 * santykius
 * žemėlapio drobės apimtis
 * projektų modeliai
 * legenda
 * mapview dokai (2D ir 3D)
 * sluoksniai su nuorodomis į pagrindinius duomenų rinkinius (duomenų šaltinius) ir kitas sluoksnio savybes, įskaitant apimtis, SRS, sujungimus, stilius, atvaizduotoją, maišymo režimą, neskaidrumą ir kt.
 * projekto savybės

### QGS aukščiausio lygio XML žymos

{{< figure src="../qgstoplevel.png" title="" >}}

### Išplėstinės aukščiausio lygio projekto sluoksnio žymos

{{< figure src="../qgstoplevel.png" title="" >}}

## Nuorodos

* [QGIS](https://www.qgis.org/en/site/)


