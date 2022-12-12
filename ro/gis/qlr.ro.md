{
  "date" : "2019-10-11",
  "keywords" :[ "fișier qlr", "format fișier qlr", "ce este un fișier qlr", "fișier", "exemplu qlr", "extensie fișier qlr", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - Fișier de definire a stratului QGIS",
  "description":"Aflați despre formatul de fișier QLR și despre API-urile care pot crea și deschide fișiere QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Ce este un fișier QLR?

Un fișier cu .qlr este un fișier de definiție a stratului care conține un indicator către sursa de date a stratului. Aceasta este în plus față de informațiile de stil [QGIS](https://www.qgis.org/en/site/) pentru strat. Având referințe la toate stilurile înrudite, acest fișier este folosit ca o singură sursă de date pentru a fi utilizate pentru obținerea informațiilor de stil. Folosind fișierele QLR, informațiile către sursele de date pot fi puse în acest singur fișier care poate fi citit de alte aplicații pentru a încărca informațiile de stil. Fișierele QLR pot fi deschise cu orice editor de text, cum ar fi Notepad++.

## Format de fișier QLR

QLR, similar cu [QGS](/ro/gis/qgs/), este un fișier XML care conține pointeri către sursa de date a stratului sub formă de etichete XML. Este similar cu fișierul ArcGIS .lyr. Etichetele de nivel superior ale unui fișier QML sunt așa cum se arată în imaginea de mai jos.

{{< figure src="../qlr.png" title="" >}}

## Referințe

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

