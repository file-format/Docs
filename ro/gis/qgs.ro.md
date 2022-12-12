{
  "date" : "2019-10-11",
  "keywords" :[ "fișier qgs", "format fișier qgs", "ce este un fișier qgs", "fișier", "exemplu qgs", "extensie fișier qgs", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Format fișier de proiect QGIS",
  "description":"Aflați despre formatul de fișier QGS și despre API-urile care pot crea și deschide fișiere QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier QGS?

Un fișier cu extensia .qgs este un fișier de proiect creat cu [QGIS](https://www.qgis.org/en/site/), care este o aplicație GIS multiplatformă open-source. Toate setările proiectului, cum ar fi proprietățile stratului și datele auxiliare pentru proiect. Este creat atunci când un proiect de hartă este salvat pe disc. Este de fapt un fișier de configurare care reține informații precum pointerii către datele GIS, informații despre stil despre straturi și titlul proiectului. Fișierele QGS pot fi deschise cu software-ul QGIS care este disponibil gratuit pentru descărcare.

## Format de fișier QGS

Fișierele QGS sunt în format [XML](/ro/web/xml/) și stochează datele proiectelor ca etichete XML. Un fișier QGS conține informații precum:

* Titlul proiectului
* proiect CRS
* arborele stratului
* setări de aprindere
* relații
* extinderea pânzei hărții
* modele de proiect
* legendă
* andocuri mapview (2D și 3D)
* straturi cu link-uri către seturile de date subiacente (surse de date) și alte proprietăți ale stratului, inclusiv extinderea, SRS, îmbinări, stiluri, redare, mod de amestecare, opacitate și multe altele.
* proprietățile proiectului

### Etichete XML de nivel superior QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Etichete de nivel superior de proiect extinse

{{< figure src="../qgstoplevel.png" title="" >}}

## Referințe

* [QGIS](https://www.qgis.org/en/site/)

