{
  "date": "2021-03-18",
  "keywords": [
"qgz failą",
"qgz failo formatas",
"kas yra qgz failas",
"failą",
"qgz pavyzdys",
"qgz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "QGZ – kvantinis GIS suspaustas projektas",
  "description": "Sužinokite apie QGZ failo formatą, kuris yra tik suspaustas QGS ir API, kurios gali kurti ir atidaryti QGZ failus.",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-ltz"
}
},
  "lastmod": "2021-03-18"
}

## Kas yra QGZ failas?

**QGZ** failo formatas yra suspaustas archyvas, kuriame yra [QGS](/gis/qgs/) failas ir QGD failas. Tuo tarpu QGD failas yra qgis projekto sqlite duomenų bazė, kurią sudaro pagalbiniai projekto duomenys. Jei nėra papildomų duomenų, QGD failas liks tuščias.

## Išsami informacija apie QGZ failo formatą

QGZ buvo pristatytas kaip naujas **QGIS 3 projekto failo formato** variantas. Šis formatas yra supakuotas QGS xml failo konteineris. Jei vartotojai pasirenka QGD, kuris yra neprivalomas formatas, tokiu atveju konteineris yra naudingas pagalbinei saugyklos duomenų bazei saugoti.

Klasikiniu režimu pagalbinė duomenų bazė išsaugoma kaip failas su plėtiniu .qgd kartu su xml failu. Renkantis supakuotą talpyklą, .qgd failas įtraukiamas į .qgz, tai tiesiog palengvina vartotoją be jokių problemų, vartotojai negali jo ištrinti arba pamiršti nukopijuoti dalindamiesi projekto failais!


## Nuorodos

* [QGZ – naujas numatytasis QGIS projekto failo formatas](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

