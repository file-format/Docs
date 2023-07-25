{
  "date" : "2019-10-11",
  "keywords" :[ "fișier gml", "ce este un fișier gml", "fișier", "exemplu gml", "extensie fișier gml", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML – Formatul de fișier al limbajului de marcare geografică",
  "description":"Aflați despre formatul de fișier GML și despre API-urile care pot crea și deschide fișiere GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GML?

GML înseamnă Geography Markup Language, care se bazează pe specificațiile XML dezvoltate de Open Geospatial Consortium (OGC). Formatul este folosit pentru a stoca caracteristici de date geografice pentru schimbul între diferite formate de fișiere. Acesta servește ca limbaj de modelare pentru sistemele geografice, precum și ca format de schimb deschis pentru tranzacțiile geografice pe internet.

## Format de fișier GML ##

Ca și în cazul majorității gramaticilor bazate pe XML, există două părți ale gramaticii – schema care descrie documentul și documentul instanță care conține datele reale. Un document GML este descris folosind o schemă GML. Acest lucru permite utilizatorilor și dezvoltatorilor să descrie seturi de date geografice generice care conțin puncte, linii și poligoane. Folosind scheme de aplicație, utilizatorii se pot referi la drumuri, autostrăzi și poduri în loc de puncte, linii și poligoane.

Este de remarcat faptul că GML nu ar trebui interpretat pentru reprezentarea datelor spațiale pe hărți. Reprezentarea conținutului GML este diferită de scopul pentru care a fost creat GML. Pe scurt, GML este similar cu XML prin faptul că este folosit doar pentru a păstra conținutul spațial care poate fi utilizat de aplicații de cartografiere în scop de afișare.

### Formarea conținutului în GML ###

GML reprezintă date spațiale folosind caracteristici care reprezintă o listă de proprietăți și geometrii. O proprietate are un nume, un tip și o descriere a valorii. Geometriile sunt compuse din blocuri de bază ale geometriei, cum ar fi:

* puncte
* linii
* curbe
* suprafeţe şi
* poligoane

Versiunile viitoare ale GML sunt planificate să accepte geometria 3D, precum și relațiile topologice dintre caracteristici.

Codarea GML permite deja funcții destul de complexe. O caracteristică poate fi compusă, de exemplu, din alte caracteristici. O singură caracteristică, cum ar fi un aeroport, ar putea fi astfel compusă din alte caracteristici, cum ar fi căi de taxi, piste, umerașe și terminale aeriene. Geometria unei caracteristici geografice poate fi, de asemenea, compusă din multe elemente de geometrie. O caracteristică complexă din punct de vedere geometric poate consta astfel dintr-un amestec de tipuri de geometrie, inclusiv puncte, șiruri de linii și poligoane.

### Exemple ###

GML 1.0 și 2.0 codifică obiectele Polygons, Points și LineString după cum urmează:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referințe ##

* [Specificații GML](https://www.ogc.org/standard/gml/)
* [GML - După Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

