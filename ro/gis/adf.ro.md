{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Format grilă binar ESRI ArcInfo",
  "description":"Aflați despre formatul de fișier ADF și despre API-urile care pot crea și deschide fișiere ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Ce este un fișier ADF?

Un fișier cu extensia .adf este un format de fișier de date raster utilizat de aplicațiile software ESRI, cum ar fi ArcGIS, ArcView și ArcInfo. Datele spațiale sunt stocate ca o grilă binară care este nativă pentru ESRI. Grila este alcătuită din rânduri și coloane de celule care pot fi întregi și virgulă mobilă. Grilele întregi dintr-un fișier ADF reprezintă date discrete, iar grilele cu virgulă mobilă reprezintă date continue. Un alt format de fișier ESRI popular este fișierul [SHP](/ro/gis/shp/) care reprezintă informații geospațiale sub formă de date vectoriale care vor fi utilizate de aplicațiile Sisteme de Informații Geografice (GIS).

## Format de fișier ADF - Mai multe informații

Fișierele ADF sunt salvate ca fișiere binare pe disc într-o grilă binară. Grilele întregi au atribute care sunt stocate într-un tabel cu atribute valorice (TVA). Fiecare valoare unică din grilă are o înregistrare în TVA unde înregistrarea stochează valoarea unică și numărul de celule din grilă este reprezentat de acea valoare.

Grilele cu virgulă mobilă nu au TVA.

### Structură grilă

În interiorul fișierului ADF, grilele sunt implementate folosind o structură de date raster. Unitatea de bază din interiorul acestei structuri de date raster este un bloc dreptunghiular de celule. Fiecare bloc este stocat pe disc și comprimat într-o structură de fișiere cu lungime variabilă, numită țigla. Fiecare bloc este stocat ca o singură înregistrare cu lungime variabilă.

Rasterele GRID sunt stocate în spații de lucru, unde un spațiu de lucru conține un subdirector de informații și un subdirector pentru fiecare GRID. Există mai multe fișiere care atribuie locație geografică și date pentru grila corespunzătoare. Subdirectorul Info conține mai multe fișiere care mențin anumite informații despre GRID și alte seturi de date, cum ar fi acoperiri, în spațiul de lucru.

## Referințe ##

* [Format grilă ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
