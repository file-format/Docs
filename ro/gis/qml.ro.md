{
  "date" : "2019-10-11",
  "keywords" :[ "fișier qml", "format fișier qml", "ce este un fișier qml", "fișier", "exemplu qml", "extensie fișier qml", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML – Formatul fișierului stil QGIS",
  "description":"Aflați despre formatul de fișier QML și despre API-urile care pot crea și deschide fișiere QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Ce este un fișier QML?

Un fișier cu extensie .qml este un fișier XML care stochează informații despre stilul straturilor pentru straturile QGIS. QGIS este o aplicație GIS multiplatformă cu sursă deschisă folosită pentru a afișa date geospațiale cu capacitatea de a organiza datele sub formă de straturi. Fișierele QML conțin informații care sunt utilizate de QGIS pentru a reda geometriile caracteristicilor, inclusiv definițiile simbolurilor, dimensiunile și rotațiile, etichetarea, opacitatea, modul de amestecare și multe altele. Spre deosebire de fișierele QLR, fișierele QML conțin toate informațiile de stil în sine. Fișierele QML pot fi deschise în orice editor de text, cum ar fi Notepad++.

## Format de fișier QML

QLR, similar cu [QGS](/ro/gis/qgs/) și [QLR](/ro/gis/qlr/), este un fișier XML care conține informații de stil pentru straturi.

Figura de mai jos arată etichetele de nivel superior ale unui fișier QML (cu doar renderer_v2 și eticheta de simbol extinsă).

{{< figure src="../qml.png" title="" >}}

## Referințe

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

