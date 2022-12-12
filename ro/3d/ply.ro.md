{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "fișier", "extensie", "format", "format fișier 3D"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier PLY și despre API-urile care pot crea și deschide fișiere PLY.",
  "title" :"PLY - Format de fișier Polygon 3D",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PLY?

PLY, Polygon File Format, reprezintă formatul de fișier 3D care stochează obiecte grafice descrise ca o colecție de poligoane. Scopul acestui format de fișier a fost de a stabili un tip de fișier simplu și ușor, care să fie suficient de general pentru a fi util pentru o gamă largă de modele. Formatul de fișier PLY vine în format ASCII și Binary pentru stocare compactă și pentru salvare și încărcare rapidă. Formatul de fișier este utilizat de diferite aplicații care oferă suport pentru citirea fișierelor 3D.

Obiectele într-un format PLY sunt descrise printr-o colecție de vârfuri, fețe și alte elemente, împreună cu proprietăți precum culoarea și direcția normală care pot fi atașate acestor elemente. Alte proprietăți care pot fi stocate împreună cu obiectul includ:

* Normale de suprafață
* coordonatele texturii
* transparenta
* interval de încredere în datele
* proprietăți pentru fața și spatele unui poligon

Un obiect reprezentat prin format PLY poate fi rezultatul diferitelor surse, cum ar fi obiecte digitalizate manual, obiecte poligonale din aplicații de modelare, date de distanță, triunghiuri din cuburi de marș, date de teren și modele de radiozitate.

## Scurt istoric

Formatul PLY a fost dezvoltat în anii 1990 de către Greg Turk și alții din laboratorul de grafică Stanford și de aceea este cunoscut și sub numele de Format Triunghi Stanford. Formatul de fișier are versiunea 1.0 de atunci și nu au mai fost făcute modificări.

## Format de fișier PLY

Un obiect PLY simplu constă dintr-o colecție de elemente pentru reprezentarea obiectului. Constă dintr-o listă de (x,y,z) triple ale unui vârf și o listă de fețe care sunt de fapt indicii în lista de vârfuri. Vârfurile și fețele sunt două exemple de elemente și majoritatea fișierului PLY constă din aceste două elemente. De asemenea, pot fi create și atașate proprietăți noi elementelor unui obiect, dar acestea ar trebui adăugate în așa fel încât programele vechi să nu se întrerupă atunci când sunt întâlnite aceste noi proprietăți. Astfel de proprietăți pot fi eliminate și prin citirea aplicațiilor. Mai mult, pot fi create elemente noi și pot fi definite proprietăți și cu acest element.

### Structura fișierului

Structura fișierului unui format de fișier PLY este următoarea:

|Câmp
---|
| Antet fișier
|Lista de vârfuri
|Lista de fețe
|Lista cu alte elemente

#### Exemplu de structură

Vom folosi următorul exemplu de mai jos în discuția noastră ulterioară pentru diferite părți ale unui format de fișier PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Antet fișier

Antetul formatului fișierului PLY constă din text ASCII atât pentru formatul ASCII, cât și pentru formatul binar. Începutul și sfârșitul secțiunii de antet sunt identificate prin cuvinte cheie pliante și antet de sfârșit. Începutul antetului are cuvântul magic ply care este folosit pentru recunoașterea formatului de fișier PLY de către cititori. Următorul rând arată numărul versiunii pentru acest fișier. Comentariile într-un format de fișier PLY încep cu cuvântul cheie comentariu la începutul fiecărei linii de comentariu.

#### Element Cuvânt cheie

Cuvântul cheie element spune apoi ce este în interiorul fișierului. Este urmată de proprietăți pentru acel tip de element specific, unde fiecare proprietate are tipul de proprietate și ordinea specificate după cum se arată mai jos:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

În acest exemplu particular, elementul de vârf specific are 3 proprietăți de tip float cu ordinea specificată.

#### Tipuri de tipuri de date

Există două tipuri de date pe care le poate avea o proprietate.

`Scalar`: Tipurile de date scalare sunt prezentate mai jos:

|#Nume|#Tip|#Număr de octeți
|caracter|caracter|1
|uchar|caracter nesemnat|1
|scurt|întreg scurt|2
|ushort|unsigned short integer|2
|int|Integer|4
|uint|unsigned Integer|4
|plutitor|plutitor cu o singură precizie|4
|dublu|plutitor de precizie dubla|8

`List`: Există o formă specială de definiții de proprietăți care utilizează tipul de date listă. Un exemplu în acest sens este din fișierul cub de mai sus:

`lista de proprietăți uchar int vertex_index`

Aceasta înseamnă că proprietatea „index_index” conține mai întâi un caracter nesemnat care spune câți indici conține proprietatea, urmat de o listă care conține atât de mulți numere întregi. Fiecare număr întreg din această listă cu lungime variabilă este un index al unui vârf.

## Referințe ##

* [Format fișier PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - După Wikipedia](https://en.wikipedia.org/wiki/PLY_(format_fișier))

