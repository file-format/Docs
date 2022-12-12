{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Comprimat", "Fișier", "Extensie", "Format fișier", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier LZO",
  "description":"Aflați despre formatul de fișier LZO și despre API-urile care pot crea și deschide fișiere LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Ce este un fișier LZO? ##

Un fișier cu extensia .lzo este combinat cu funcții de arhivare a fișierelor care pot reduce dimensiunea tuturor fișierelor din fișierul comprimat. Toate fișierele comprimate pot cuprinde unul sau mai multe fișiere sau chiar grupuri de liere cu mai multe fișiere de diferite tipuri și dimensiuni. Dimensiunea unui fișier comprimat este mai mică în comparație cu dimensiunea comună a tuturor fișierelor și folderelor stocate într-un fișier comprimat LZO. Toate fișierele comprimate LZO sunt stocate în format LZO și sunt executate în mod explicit cu caracteristicile de compresie utilizate de software-ul de compresie și decompresie a fișierelor LZOP. Toate specificațiile de compresie sunt combinate în acest program de compresie și decompresie a fișierelor care provine din biblioteca de compresie a fișierelor Lempel-Ziv-Oberhume. Viteza de decompresie mai mare și rapoartele de compresie dezvoltate sunt, de asemenea, combinate în aceste fișiere LZO.

## Specificație LZO ##

Markus Franz Xaver Johannes Oberhumer a dezvoltat algoritmul original „lzop”, bazat pe algoritmi anteriori de Abraham Lempel și Jacob Ziv, în 1996. Această bibliotecă implementează o varietate de algoritmi cu următoarele caracteristici:

* Compresie mai rapidă decât DEFLATE
* Decompresie rapidă
* Buffer-uri suplimentare care sunt necesare în timpul compresiei (de dimensiune de 8 KB sau 64 KB, în funcție de nivelul de compresie)
* Bufferele sursă și destinație sunt toată memoria necesară pentru decompresie
* Oferă control atât asupra raportului de compresie, cât și asupra vitezei de compresie

Ca algoritm de compresie bloc, LZO efectuează compresie suprapusă, precum și decompresie în loc. Pentru a obține compresia suprapusă, dimensiunea blocului atât a compresiei, cât și a decompresiei trebuie să se potrivească. Algoritmul de compresie LZO împarte datele de intrare în potriviri (un dicționar glisant) și literale care nu se potrivesc, oferind rezultate bune cu date extrem de redundante și rezultate acceptabile cu date necompresibile, crescând doar datele incompresibile cu 1/64 din originalul mărimea.

## Probleme la deschiderea unui fișier LZO ##

Următoarele sunt câteva probleme care pot cauza funcționarea proastă a formatului de fișier LZO:
  


* Fișierul poate fi corupt. Pentru a rezolva această problemă, descărcați din nou fișierul sau cereți expeditorului să retrimite fișierul din nou
* Al doilea motiv este fișierul infectat, în acest caz, scanați fișierul corect
* Legături necorespunzătoare către fișierul LZO
* Eliminarea descrierii LZO
* Nu sunt suficiente resurse hardware
* Șoferi de echipamente învechiți
  


## Referințe ##

* [LZO - Prin Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

