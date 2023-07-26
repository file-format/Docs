{
  "date" : "2021-07-29",
  "keywords" :[ "fișier shx", "format fișier shx", "ce este un fișier shx", "fișier", "exemplu shx", "extensie fișier shx", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Formatul index al formei Shapefile",
  "description":"Aflați despre formatul de fișier SHX și despre API-urile care pot crea și deschide fișiere SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Ce este un fișier SHX?
Fișierul SHX aparține formatului de index de formă, care este un index de poziție al geometriei caracteristicii pentru a permite căutarea rapidă înainte și înapoi. SHX este un fișier offset cu acces direct. Nu există date în acest fișier, ci doar o copie duplicată a primei sute de octeți, numărul înregistrării și offset față de octetul de început al acelei înregistrări în shp. Vă rugăm să rețineți că fișierul cu extensia .shx nu leagă [SHP](/ro/gis/shp/) și [DBF](/ro/database/dbf).

## Format de fișier SHX
Formatul SHX conține indexul pozițional al geometriei caracteristicii și antetul de 100 de octeți similar fișierului SHP, urmat de orice număr de înregistrări de lungime fixă de 8 octeți care conțin următoarele două câmpuri:
| Octeți | Tip | Endianness | Utilizare |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | mare | Înregistrare offset (în cuvinte de 16 biți) |
| 4–7 | int32 | mare | Lungimea înregistrării (în cuvinte de 16 biți) |

Acest index face posibilă căutarea înapoi în fișierul de formă, mai întâi, căutând înapoi în indexul formei și apoi citind offset-ul înregistrării. Acest offset poate fi folosit pentru a căuta poziția corectă în fișierul SHP. De asemenea, puteți căuta înainte; un număr arbitrar de înregistrări folosind aceeași metodă. Deși, este posibil să generați un index complet împreună cu un fișier SHP, dar poate crește șansele de a face fișierul SHP corupt rapid.


## Referințe

* [Shapefile - de la Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)


