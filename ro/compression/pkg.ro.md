{
  "date" : "2021-04-08",
  "keywords" :[ "fișier pkg", "format fișier pkg", "ce este un fișier pkg", "fișier", "exemplu pkg", "extensie fișier pkg", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Format de fișier arhivă extensibil",
  "description":"Aflați despre formatul de fișier PKG și despre API-urile care pot crea și deschide fișiere PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Ce este un fișier PKG?

Un fișier cu extensia .pkg este un fișier de pachet de instalare care este utilizat pentru a instala software-ul pe macOS. Pe lângă computerele Macintosh, este folosit și pe iPhone. Aplicația de instalare Apple încorporată poate fi utilizată pentru a instala conținutul unui fișier PKG. Un fișier PKG este similar cu un fișier MSI utilizat pe sistemul de operare Windows pentru instalarea software-ului. În timpul instalării, aceste fișiere de pachete pot înregistra mesaje care vă oferă o idee ce lucruri suplimentare sunt instalate de acest pachet.

## Format de fișier PKG

PKR sunt fișiere binare care sunt comprimate pentru a reduce dimensiunea totală a fișierului. Începând cu OSX 10.5, pachetele plate cu fișiere de instalare unice au fost introduse de Apple. Acestea sunt diferite de formatele de ambalare anterioare care au venit ca pachete, mai degrabă decât fișiere individuale. Aceste pachete incluse au conținut o ierarhie de directoare structurată care stoca fișiere într-un mod care facilitează recuperarea lor prin intermediul unui fișier index. Formatul de fișier PKG plat este de fapt o arhivă [XAR](/ro/compression/xar/) care are:

* Antet - Definește dimensiunea, suma de control și informațiile despre versiune
* Cuprins - Un document XML care este (și trebuie) codificat ca UTF-8 și este stocat la începutul fișierului, facilitând scanarea prin arhivă pentru a extrage fișierul individual
* Heap - grămada nestructurată de date la care face referire TOC

## Referințe

* [Format de fișier pachet plat](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

