{
  "date" : "2021-03-18",
  "keywords" :[ "fișier qgz", "format fișier qgz", "ce este un fișier qgz", "fișier", "exemplu qgz", "extensie fișier qgz", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Proiect comprimat GIS cuantic",
  "description":"Aflați despre formatul de fișier QGZ, care este doar un QGS comprimat și API-uri care pot crea și deschide fișiere QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Ce este un fișier QGZ?

Formatul de fișier **QGZ** este o arhivă comprimată care conține un fișier [QGS](https://docs.fileformat.com/gis/qgs/) și un fișier QGD. Întrucât, fișierul QGD este baza de date sqlite a proiectului qgis care constă din date auxiliare pentru proiect. Dacă nu există date auxiliare, fișierul QGD va rămâne gol.

## Detalii despre formatul fișierului QGZ

QGZ a fost introdus ca o nouă variantă a **formatului de fișier de proiect QGIS 3**. Acest format este un container arhivat pentru fișierul xml QGS. Dacă utilizatorii aleg QGD care este un format opțional, în acest caz containerul este benefic pentru stocarea bazei de date auxiliare de stocare.

În modul clasic, baza de date auxiliară este salvată ca fișier cu extensia .qgd de-a lungul fișierului xml. Atunci când alegeți containerul arhivat, fișierul .qgd este inclus în .qgz, pur și simplu facilitează utilizatorii fără nicio problemă, utilizatorii nu îl pot șterge sau uita să-l copieze atunci când partajează fișiere de proiect!


## Referințe

* [QGZ – Un nou format implicit de fișier de proiect pentru QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formate de fișiere QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

