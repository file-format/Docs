{
  "date" : "2019-12-12",
  "keywords" :[ "DB3", "DB3 File Format", "DB3 File", "SQLite", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date" ] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DB3 și despre API-urile care pot crea și deschide fișiere DB3.",
  "title" :"Format fișier DB3",
  "linktitle" : "DB3",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Ce este un fișier DB3?
Fișierul DB3 este un fișier de bază de date creat de software-ul SQLite, care este un program de bază de date ușor, autonom, care creează baze de date folosind fișiere simple; conține anatomia bazei de date, precum și înregistrările de date; utilizat în mod obișnuit pentru preluarea sau stocarea datelor structurate folosind SQL. Aceste fișiere pot fi utilizate în dispozitive inteligente sau acolo unde este necesară păstrarea înregistrărilor sau alte gestionări a datelor, dar într-un mediu cu spațiu redus.


## Format de fișier DB3
Formatul de fișier DB3 este asociat cu RDBMS (Relational Database Management System) SQLite, o alegere populară pentru bazele de date încorporate. Nu există nicio extensie de fișier specifică definită într-un SQLite_3 în specificația sa, acesta poate folosi extensii, inclusiv [.dbf](/ro/database/dbf/) și [.sqlite](/ro/database/sqlite/).

### Secificarea bazei de date
În mod obișnuit, formatul de fișier db legat de SQLite, versiunea 3, poate fi considerat formatul de fișier DB3 utilizat ca format nativ documentat public pentru motorul de baze de date SQLite din iunie 2004. Formatul de fișier DB3 este o platformă multiplatformă, transferabil între big-endian și arhitecturi little-endian sau sisteme pe 32 și 64 de biți. Aceste caracteristici fac din DB3 o alegere populară ca format de fișier de aplicație. Fișierul principal al bazei de date SQLite_3 (DB3) este format din una sau mai multe pagini. Toate dimensiunile tuturor paginilor sunt egale în aceeași bază de date. Dimensiunea paginii în octeți este o putere de doi între 512 și 65536 inclusiv.



## Referințe ##

* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite, Versiunea 3](https://www.loc.gov/preservation/digital/formats/fdd/fdd000461.shtml)

