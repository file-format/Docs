{
  "date": "2021-03-18",
  "author": {
    "display_name": "Muhammad Umar",
    "keywords": [
"QGD",
"QGIS projekta Sqlite datu bāze",
"pagarinājumu",
"formātā",
"QGIS",
"Papildu datu bāze",
"Kas ir QGD fails"
]
},
  "draft": "false",
  "toc": true,
  "title": "QGD — QGIS projekta Sqlite datu bāze",
  "description": "Uzziniet par QGD, kas ir QGIS projekta sqlite datu bāze un API, kas var izveidot un atvērt QGD failus.",
  "linktitle": "QGD",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-lvd"
}
},
  "lastmod": "2021-03-18"
}

## Kas ir QGD fails?

Fails ar paplašinājumu .QGD fails faktiski ir **QGIS** projekta saistītā sqlite datu bāze, kurā ir iekļauti projekta palīgdati. QGD fails paliks tukšs, ja projektam nebūs papildu datu.

## Sīkāka informācija par QGD faila formātu

Klasiskajā režīmā papildu datu bāze tiek saglabāta kā fails ar paplašinājumu .qgd kopā ar xml failu. Sistēma **Auxiliary Database** ļauj nolasīt un rakstīt datus sistēmā kā alternatīvu veidu. Veidojot QGZ, kas ir zip konteiners, .qgd fails tiek iekļauts .qgz.

## Kas ir papildu datu bāze?
Papildu datu bāze faktiski ir gaidstāves db sistēma, kas tiek izveidota kā atbilde uz mērķa datu bāzes dublēšanos. Papildu datu bāze faktiski ir dublikāta gadījumā datu bāze, kurā veicat dublēšanu. Piemēram, ja iestatāt gaidstāves datu bāzi, izmantojot dublikātu datu bāzi, avota datu bāze būs mērķis un gaidstāves datu bāze tiks dēvēta par papildu datu bāzi.


## Atsauces

* [QGZ — jauns noklusējuma projekta faila formāts QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

