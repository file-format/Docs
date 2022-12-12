{
  "date" : "2019-10-11",
  "keywords" :[ "fișier shp", "format fișier shp", "ce este un fișier shp", "fișier", "exemplu shp", "extensie fișier shp", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Aflați despre formatul de fișier SHP și despre API-urile care pot crea și deschide fișiere SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier SHP?

SHP este extensia de fișier pentru unul dintre tipurile de fișiere principale utilizate pentru reprezentarea ESRI Shapefile. Reprezintă informații geospațiale sub formă de date vectoriale pentru a fi utilizate de aplicațiile Sisteme de Informații Geografice (GIS). Formatul a fost dezvoltat ca specificații deschise pentru a facilita interoperabilitatea între ESRI și alte produse software.

## Reprezentarea datelor

După cum sa menționat, un format de fișier de formă descrie informațiile geospațiale ale unui set de date ca caracteristici vectoriale. Aceste caracteristici vectoriale includ:

* puncte
* linii
* poligoane

Aceste caracteristici în combinație pot reprezenta aproape orice tip de forme, cum ar fi fântâni de apă, limite de țară, puncte spațiale, debitul râurilor, lacuri, etc. Fiecare caracteristică vectorială poate avea atribute care definesc de fapt scopul acelei caracteristici. De exemplu, un shapefile care conține orașe din Los Angeles poate avea numele orașului și temperatura ca atribute care oferă o reprezentare semnificativă a datelor spațiale.

## Fișiere asociate

Un fișier shp de sine stătător nu poate fi folosit de aplicațiile software pentru a da sens datelor pe care le conține. Pentru a înțelege informațiile conținute într-un astfel de fișier, un shapefile utilizează următoarele fișiere obligatorii suplimentare.

* fișier shx - fișier index
* fișier dbf - un fișier dBASE care stochează toate atributele formelor din fișierul principal
* fișier prj - stochează informațiile despre proiect ale fișierului

Pot exista și alte fișiere opționale care au același nume ca fișierul principal.

## Specificații pentru formatul fișierului SHP

Specificațiile deschise ale shapefile sunt disponibile online de la ESRI sub formă de [Descriere tehnică](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) și elaborează structura generală a fișierului în detaliu. Informațiile din fișierul principal .shp sunt formate din anteturi și înregistrări. Antetul fișierului cu lungime fixă este urmat de înregistrări cu lungime variabilă, unde fiecare înregistrare este alcătuită dintr-un antet cu lungime fixă urmat de conținutul înregistrării cu lungime variabilă.

### Antet principal al fișierului SHP

Antetul principal al fișierului începe de la începutul fișierului și are o lungime de 100 de octeți. Organizarea acestui antet principal al fișierului împreună cu poziția octetilor, valoarea, tipul și ordinea octeților este așa cum se arată în tabelul următor.


|Octeți|Câmp|Valoare|Tip|Ordine octet
---|---|---|---|---|
|0-3|Cod fișier|9994|Integer|Big Endian
|4-23|Neutilizat|0|Integer|Big Endian
|24-27|Lungimea fișierului|Lungimea fișierului|Integer|Big Endian
|28-31|Versiune|1000|Integer|Little Endian
|32-35|Tip de formă|Tip de formă|Întreg|Little Endian
|36-67|Dreptunghi de limite minime|Xmin, Ymin, Xmax și Ymax|dublu|Little Endian
|68-83|Boounding Box|Zmin, Zmax|dublu|Little Endian
|84-99|Casa de delimitare|Mmin, Mmax|dublu|

Este de remarcat faptul că valoarea lungimii fișierului este lungimea totală a fișierului în cuvinte de 16 biți care include și cele cincizeci de cuvinte de 16 biți care formează antetul.

#### Tipuri de forme

Valorile câmpului tipurilor de formă din tabelul de mai sus sunt după cum urmează:


|Valoare|Tip de formă
---|---|
|0|Formă nulă
|1|Punctul
|3|Polilinie
|5|Poligon
|8|Multipunct
|11|PunctulZ
|13|PolyLineZ
|15|PoligonZ
|18|MultiPointZ
|21|PunctulM
|23|PolyLineM
|25|PoligonM
|28|MultiPointM
|31|MultiPatch

### Înregistrări de date ###

Antetul fișierului principal este urmat de înregistrări cu lungime variabilă, unde fiecare înregistrare constă dintr-un antet de înregistrare cu lungime fixă urmat de conținutul înregistrării cu lungime variabilă.

#### Antet înregistrare ####

Antetul înregistrării conține informații despre numărul înregistrării și lungimea conținutului înregistrării într-o lungime fixă de 8 octeți. Organizarea antetului înregistrării este după cum urmează:


|Octeți|Câmp|Valoare|Tip|Ordine octet
---|---|---|---|---|
|0-3|Număr înregistrare|Număr înregistrare|Întreg|Mare
|4-7|Lungimea înregistrării|Lungimea înregistrării|Integer|Mare

#### Înregistrați conținutul ####

Conținutul unei înregistrări de fișier de formă este format dintr-un tip de formă urmat de datele geometrice pentru acea formă. Un tip de formă de 0 reprezintă o formă nulă care nu are date geometrice pentru formă. Lungimea conținutului înregistrării este reflectarea părților de formă și a vârfurilor. Să luăm un exemplu de tip Point Shape pentru a elabora modul în care o înregistrare conține informații despre un astfel de tip de formă.

Un punct reprezintă o anumită locație geografică în ordinea X,Y unde fiecare coordonată este reprezentată printr-o valoare de dublă precizie. Următorul tabel arată aranjamentul unui tip de formă Punct.


|Octeți|Tip de formă|Valoare|Tip|Număr|Ordine de octeți
---|---|---|---|---|---|
|0-3|Tip de formă|1|Întreg|1|Mic
|4-11|X|X|dublu|1|Mic
|12-19|Y|Y|double|1|Mic

Exemple de alte tipuri de forme pot fi găsite în documentul de descriere tehnică ESRI.

## Referințe ##

* [ESRI Shapefile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) de către ESRI

