{
  "date" : "2022-03-21",
  "keywords" :[ "fișier xpr", "format fișier xpr", "ce este un fișier xpr", "fișier", "exemplu xpr", "extensie fișier xpr", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier XPR - Fișier grafic Microsoft Expression Design",
  "description":"Aflați despre formatul de fișier XPR și despre API-urile care pot crea și deschide fișiere XPR.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Ce este un fișier XPR?

Un fișier XPR este un fișier de imagine vectorială creat cu software-ul Microsoft Expression Graphics (EGD), întrerupt acum. Conține informații grafice care pot fi folosite ca model de interfață cu utilizatorul. Fișierele XPR au fost ulterior înlocuite cu fișiere .design în Microsoft Expression Design. Fișierele XPR ar putea fi deschise cu Microsoft Expression Studio, care a fost întrerupt de ceva timp.

## Vulnerabilitatea formatului fișierului XPR

Fișierele XPR au fost identificate pentru a beneficia de o vulnerabilitate în Microsoft Expression Design, ceea ce duce la permiterea executării codului de la distanță. În problema raportată, dacă un utilizator a deschis un fișier .xpr legitim care este acoperit în directorul de rețea împreună cu fișierul DLL (Dynamic Link Library), Microsoft Expression Design ar putea încerca să încarce fișierul DLL și să execute codul pe care îl conține. Acest lucru a fost remediat ulterior de Microsoft într-o actualizare de securitate.

## Referințe

* [Vulnerabilitatea în designul expresiei ar putea permite executarea codului de la distanță (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

