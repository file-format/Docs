{
  "date" : "2020-03-16",
  "keywords" :[ "Fișier STL", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier STL și despre API-urile care pot crea și deschide fișiere STL.",
  "title" :"Format fișier STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este fișierul STL?

STL, abrevierea pentru stereolitrografie, este un format de fișier interschimbabil care reprezintă geometria suprafeței tridimensionale. Formatul de fișier își găsește utilizarea în mai multe domenii, cum ar fi prototiparea rapidă, imprimarea 3D și fabricarea asistată de computer. Reprezintă o suprafață ca o serie de triunghiuri mici, cunoscute sub numele de fațete, unde fiecare fațetă este descrisă printr-o direcție perpendiculară și trei puncte reprezentând vârfurile triunghiului. Datele rezultate sunt utilizate de aplicații pentru a determina secțiunea transversală a formei 3D care urmează să fie construită de către fabber. Nu există informații disponibile în formatul de fișier STL pentru reprezentarea culorii, texturii sau a altor atribute comune ale modelului [CAD](/ro/cad/).

## Scurt istoric ##

Dezvoltarea formatului de fișier STL datează din 1987. A fost dezvoltat de 3D Systems pentru utilizarea sa în imprimante 3D comerciale. O versiune revizuită a formatului de fișier STL, cunoscută sub numele de STL 2.0, a fost propusă în 2009, cu actualizări ale formatului de fișier.

## Specificații de format de fișier ##

Un fișier STL reprezintă o geometrie a suprafeței folosind fațete. Fațetele definesc suprafața unui obiect 3D și sunt identificate în mod unic printr-o normală unitară, care este o linie perpendiculară pe triunghiul cu lungimea de 1,0 și prin trei vârfuri. Există un total de 12 numere stocate pentru fiecare fațetă ca Normal și fiecare vârf este specificat de trei coordonate fiecare. Fișierul StL nu conține nicio informație de scară; coordonatele sunt în unități arbitrare.

Specificațiile formatului de fișier STL pot fi examinate din următoarele două aspecte.

### Orientare fațete ###

Orientarea unei fațete este determinată de direcția normalei unității și de ordinea în care sunt listate vârfurile. Orientarea fațetelor este specificată în două moduri, după cum urmează:

* Direcția normalului este spre exterior
* Vârfurile sunt listate în ordinea inversă a acelor de ceasornic din exterior, respectând regula mâinii drepte.

### Regula vârf la vârf ###

Conform acestei reguli, fiecare triunghi împarte două vârfuri cu fiecare dintre triunghiurile sale adiacente. Astfel, un vârf al unui triunghi nu poate fi situat pe latura altui triunghi.

## Formate de fișiere ##

STL este disponibil în ASCII, precum și în reprezentări binare pentru format de fișier compact.

### Format STL ASCII ###

Versiunea ASCII a formatului de fișier STL este scrisă în ASCII simplu. Cu toate acestea, din cauza dimensiunii sale mari, formatul de fișier nu este selectat ca format preferat pentru utilizare. Sintaxa unui fișier ASCII STL este următoarea:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Cuvintele aldine reprezintă cuvinte cheie care ar trebui să fie întotdeauna cu litere mici. Simbolurile cu caractere cursive sunt variabile care trebuie înlocuite cu valori specificate de utilizator. Datele numerice din liniile **normală fațetă** și **vertix** sunt flotanți de precizie unică, de exemplu, 1,23456E+789. O coordonată **fațetă normală** poate avea semnul minus la început; o coordonată **vertex** nu poate.

### Format binar STL ###

Formatul binar folosește reprezentarea numerică IEEE întreg și în virgulă mobilă. Formatul fișierului este reprezentat după cum urmează:

|Câmp|Informații|
---|---|
|Header|80 caractere|
|Număr de triunghiuri|întreg fără semn Little Endian de 4 octeți|
|Date pentru fiecare triunghi|12 numere în virgulă mobilă pe 32 de biți|

O vedere mai elaborată a formatului de fișier este prezentată mai jos.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referințe ##

* [Formatul STL](http://www.fabbers.com/tech/STL_Format)
* [STL - de Wikipedia](https://en.wikipedia.org/wiki/STL_(format_fișier))

