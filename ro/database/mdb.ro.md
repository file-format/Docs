{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier MDB și despre API-urile care pot crea și deschide fișiere MDB.",
  "title" :"Format de fișier MDB - Un fișier de bază de date Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Ce este un fișier MDB?

Un fișier cu extensia .mdb este un fișier de bază de date Microsoft Access care este un sistem de gestionare a bazelor de date relaționale (RDBMS). Stochează date în tabele de baze de date care sunt legate între ele prin chei primare și străine. Fișierul MDB conține structura completă a tabelelor bazei de date, interogări, proceduri stocate. MDB este formatul de fișier implicit pentru Microsoft Access 2003. Versiunile laterale ale Microsoft Access utilizează formatele de fișier [ACCDB](/ro/database/accdb/), care este cel mai recent format de fișier de până acum. Fișierele MDB pot fi deschise cu aplicații precum Microsoft Access, MDB Viewer, MDBOpener și pot fi convertite în formate ACCDB, [CSV](/ro/spreadsheet/csv/), Excel etc.

## Format de fișier MDB

Există specificații publice disponibile pentru formatul MDB și acesta rămâne formatul de fișier proprietar al Microsoft. Cu toate acestea, Microsoft oferă acces la conectivitate la fișierul MDB utilizând standardul Open Database Connectivity (ODBC) și Visual Basic for Applications (VBA). Ghidul neoficial MDB oferă o scurtă descriere informală a formatului MDB bazată pe inginerie inversă și poate fi consultat pentru a cunoaște specificațiile.

### pagini

Conform ghidului neoficial MDB, un fișier MDB constă din pagini de dimensiune fixă (2048 octeți pentru Jeb DB3 și 4096 octeți pentru Jet DB 4). Primul octet indică tipul paginii. Următoarele sunt principalele tipuri de pagini:

`Prima pagină:` conține informații despre antetul bazei de date care include și identificarea versiunii Jet DB cu care fișierul este compatibil. În plus, include și informații despre securitatea fișierelor și o hartă a utilizării paginii.

`Pagină de definire a tabelului:` O pagină de definire a tabelului specifică coloanele, tipurile de date, indexul și alte informații. Folosește pagini suplimentare dacă este necesar și include o hartă a paginilor care conține datele rând pentru acest tabel.

`Pagini de date:` Paginile de date sunt containerele de date reale în care datele sunt stocate pe rânduri. Folosește pagini subsidiare pentru a stoca valori lungi de date.

O singură bază de date Microsoft Access poate cuprinde mai multe fișiere care permit depășirea limitelor de dimensiune a fișierelor și a tabelelor. Acest lucru facilitează introducerea formularelor și a codului într-un fișier MDB front-end pe desktopul utilizatorului și a datelor în alte fișiere MDB backend pe servere conectate la rețea.

## Referințe ##

* [Specificații de acces](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
