{
  "date": "2021-03-18",
  "keywords": [
"qgz fails",
"qgz faila formāts",
"kas ir qgz fails",
"failu",
"qgz piemērs",
"qgz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "QGZ - Quantum GIS saspiests projekts",
  "description": "Uzziniet par QGZ faila formātu, kas ir tikai saspiests QGS un API, kas var izveidot un atvērt QGZ failus.",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-lvz"
}
},
  "lastmod": "2021-03-18"
}

## Kas ir QGZ fails?

Faila formāts **QGZ** ir saspiests arhīvs, kas satur [QGS](/gis/qgs/) failu un QGD failu. Savukārt QGD fails ir qgis projekta sqlite datu bāze, kas sastāv no projekta palīgdatiem. Ja nav papildu datu, QGD fails paliks tukšs.

## Sīkāka informācija par QGZ faila formātu

QGZ tika ieviests kā jauns **QGIS 3 projekta faila formāta** variants. Šis formāts ir zip konteiners QGS xml failam. Ja lietotāji izvēlas QGD, kas ir neobligāts formāts, šajā gadījumā konteiners ir izdevīgs papildu krātuves datu bāzes glabāšanai.

Klasiskajā režīmā papildu datu bāze tiek saglabāta kā fails ar paplašinājumu .qgd kopā ar xml failu. Izvēloties zip konteineru, .qgd fails tiek iekļauts .qgz, tas vienkārši atvieglo lietotājus bez problēmām, lietotāji nevar to izdzēst vai aizmirst to kopēt, kopīgojot projekta failus!


## Atsauces

* [QGZ — jauns noklusējuma projekta faila formāts QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

