{
  "date" : "2021-07-29",
  "keywords" :[ "fișier gpkg", "format fișier gpkg", "ce este un fișier gpkg", "fișier", "exemplu gpkg", "extensie fișier gpkg", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - Fișiere în format GeoPackage",
  "description":"Aflați despre formatul de fișier GPKG și despre API-urile care pot crea și deschide fișiere GPKG.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Ce este un fișier GPKG?
Un fișier cu extensia .gpkg constă dintr-un sistem de informații geografice implementat ca un container de bază de date SQLite care conține date și tabele de metadate cu definiții tipice, limitări de format, afirmații de integritate și constrângeri de conținut. A fost publicată în 2014; definit de OGC (Open Geospatial Consortium) în numele armatei SUA. Diverse guverne, organizații comerciale și open source sprijină pe scară largă GeoPackage.

## Format de fișier GPKG
Un GeoPackage este alcătuit ca un fișier de bază de date SQLite 3 extins; un standard definește un set de reguli (convenții obligatorii) pentru:
- Stocarea seturi de imagini cu matrice de plăci
- Caracteristici vectoriale
- Hărți raster la diferite scări
- Metadate și schemă

Puteți extinde un GeoPackage utilizând regulile de extensie așa cum sunt definite în clauza 2.3 a standardului. Scopul proiectării unui GeoPackage a fost de a realiza o bază de date ușoară cât mai mult posibil și de a o include într-un singur fișier gata de utilizat. Acest lucru îl face ideal pentru aplicații mobile în modul off-line și partajare rapidă pe stocare în cloud sau dispozitive de stocare USB etc.

### GPKG Conținut
GeoPackage-urile conțin un număr de tabele, ca și alte baze de date relaționale. Aceste tabele pot fi fie definite de utilizator, fie tabele cu metadate. GeoPachetele constau din două tabele de metadate obligatorii:

#### gpkg_contents
Un cuprins pentru un GeoPackage. Coloanele obligatorii din acest tabel sunt:

- **table_name**: numele real al tabelului de date definit de utilizator;
- **data_type**: tipul de date, de exemplu titluri, caracteristici și atribute;
- **identificator și descriere**: text care poate fi citit de om ;
- **last_change**: data informativă a ultimei modificări, în format ISO 8601 ;
- **min_x, min_y, max_x și max_y**: extinderile spațiale ale conținutului. ;
- **srs_id**: sistem de referință spațială .

#### gpkg_spatial_ref_sys
Pentru conținut de referință spațială; inclusiv, dar fără a se limita la plăci și caracteristici, fiecare rând din conținut trebuie să facă referire la un sistem de referință de coordonate; stocate în tabelul **gpkg_spatial_ref_sys**. Coloanele obligatorii din acest tabel sunt:

- **srs_name, description**: un nume și o descriere care pot fi citite de om pentru SRS;
- **srs_id**: un identificator unic pentru SRS; de asemenea, cheia primară pentru tabel;
- **organizație**: numele organizației care nu ține seama de majuscule și minuscule.
- **organization_coordsys_id**: ID-ul numeric al SRS-ului atribuit de organizație;
- **definiție**: definiția textului bine cunoscut a SRS.


## Referințe

* [GeoPackage - de la Wikipedia](https://en.wikipedia.org/wiki/GeoPackage)
* [Noțiuni introductive despre GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

