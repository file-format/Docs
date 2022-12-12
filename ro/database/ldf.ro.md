{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier LDF și despre API-urile care pot crea și deschide fișiere LDF.",
  "title" :"LDF - Formatul fișierului bazei de date master SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Ce este un fișier LDF?

Un fișier cu extensia .ldf este un fișier jurnal menținut de Microsoft SQL Server, care este un sistem de gestionare a bazelor de date relaționale (RDBMS). Toate tranzacțiile efectuate pe fișierele bazei de date primare ([MDF](/ro/database/mdf/)) (cum ar fi inserarea, actualizarea, ștergerea) sunt înregistrate în fișierul LDF. Fișierele LDF sunt componente critice ale oricărei baze de date. În cazul unei defecțiuni a sistemului, fișierul jurnal este utilizat pentru a restabili baza de date la o stare consecventă. Fișierul jurnal de tranzacții poate crește în dimensiune dacă tranzacțiile nu sunt complet angajate. Fișierele LDF pot fi deschise cu aplicația software Microsoft SQL Server.

## Operațiuni înregistrate în fișierul LDF

Un fișier jurnal SQL înregistrează următoarele operații:

* Începutul și sfârșitul fiecărei tranzacții.

* Fiecare modificare a datelor (inserați, actualizați sau ștergeți). Aceasta include, de asemenea, modificări ale procedurilor stocate de sistem sau ale instrucțiunilor DDL (Data Definition Language) la orice tabel, inclusiv tabelele de sistem.

* Fiecare extensie și alocare sau dezalocare de pagină.

* Crearea sau eliminarea unui tabel sau index.

## Format de fișier LDF

Fișierul LDF constă din înregistrări ale tranzacțiilor SQL Server care sunt aranjate ca șir de înregistrări de jurnal. Fiecare înregistrare de jurnal are un număr de secvență de jurnal (LSN) care este mai mare decât LSN-ul înregistrării anterioare. Șirurile sunt concatenate unul după altul în fișier. Datorită computerelor moderne de mare viteză, înregistrările pot fi inserate acolo unde LSN2 există în fișierul jurnal înainte de LSN1. Deoarece operațiunile sunt înregistrate într-un serial, modificarea descrisă de LSN2 a fost efectuată după înregistrarea de jurnal LSN1. Înregistrările pentru o anumită tranzacție sunt legate înapoi folosind pointerii care sunt utilizați și accelerează derularea tranzacției.
 

## Referințe

* [Fișiere și grupuri de fișiere baze de date](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Ghid de arhitectură și management al jurnalului de tranzacții](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- server-ver15)

