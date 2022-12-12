{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extensie", "fișier", "format fișier", "Tipul fișierului bazei de date", "Format fișierului bazei de date", "Btrieve Database"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier BTR și despre API-urile care pot crea și deschide fișiere BTR.",
  "title" :"BTR - Fișierul bazei de date Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Ce este un fișier BTR?

Un fișier cu extensia .btr este un fișier de bază de date creat de [Btrieve](https://www.actian.com/) aplicația de bază de date tranzacțională. Spre deosebire de sistemele de management al bazelor de date relaționale (RBMS), Btrieve se bazează pe Metoda de acces secvențial indexat (ISAM), care este o modalitate de stocare a datelor pentru o recuperare rapidă. Fișierul BTR stochează o colecție de înregistrări și este utilizat pentru a genera rapoarte conform cerințelor. Fișierele BTR pot fi deschise folosind Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility și Legend Software BTRIEVE Viewer.

## Structura fișierului BTR - Mai multe informații

Structura internă a datelor și alinierea fiecărui octet în structura unui fișier BTR nu sunt disponibile public. Cu toate acestea, Btrieve
furnizează [API-ul Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) care poate fi folosit pentru a citi informațiile din fișierele BTR. Este compatibil cu următoarele limbaje de programare și medii de dezvoltare.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Preluarea datelor dintr-un fișier BTR depinde de fișierul DDF asociat cu acesta. Fără DDF, nu va fi ușor să recuperați informațiile dintr-un astfel de fișier.

## Referințe

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introducere în API-urile Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

