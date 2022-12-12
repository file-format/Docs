{
  "date" : "2021-08-24",
  "keywords" :[ "fișier wdb", "format fișier wdb", "ce este un fișier wdb", "fișier", "exemplu wdb", "extensie fișier wdb", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier WDB și despre API-urile care pot crea și deschide fișiere WDB.",
  "title" :"WDB - Fișier de urmărire SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Ce este un fișier WDB?
Un fișier cu extensia .wdb este de fapt un fișier de bază de date creat de Microsoft Works care a fost folosit pentru a îndeplini funcții precum un sistem de gestionare a bazelor de date. Fișierul WDB este similar cu fișierul Access Database ([MDB](/ro/database/mdb/)), dar mai puțin eficient și limitări mai mari. Fișierele WDB nu pot fi deschise utilizând Microsoft Access. Cu toate acestea, puteți deschide fișierul WDB în Microsoft Works și apoi îl puteți exporta în fișierul MDB, pentru a deschide un fișier WDB în MS Access.

## Format de fișier WDB
Baza de date Microsoft Works este formatul de bază de date nativ al suitei de birou Microsoft Works. Din cauza naturii proprietare a formatului și a unor limitări. Fișierele WDB nu pot fi deschise în niciun alt software decât Microsoft Works. În formatul de fișier, un antet recurent de 10 octeți poate fi găsit înaintea fiecărui șir de text ASCII reprezentând valorile câmpurilor care au fost terminate cu o valoare NULL. Antetul începe în general cu un octet **\x0f** și NULL, urmat de 4 octeți de date alternați cu NULL.

### Structura fișierului

Structura fișierului WDB este prezentată mai jos:
- **Primul antet**: de la începutul fișierului, se termină cu \x25\x00\xf2 și 244 de octeți NULL
- **Al doilea antet**: începe cu \xffT - adică \xff\x54 și se extinde pe 4096 de octeți, care conține nume de coloane/câmpuri și alte lucruri și pare să înceapă la poziția octet 6144.
- **Câmp**: valoarea are un antet de 10 octeți, cu următorul format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3} , partea 2} {db 4} \x00. octetul de date 2 este numărul câmpului, octetul de date 3 este numărul de înregistrare (adăugând octetul de date 3, partea 2 când trece peste 256 de înregistrări).


## Referințe ##

* [Utilizator:JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

