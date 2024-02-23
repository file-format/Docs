{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aflați despre formatul de fișier DSN și despre API-urile care pot crea și deschide fișiere DSN.",
  "title" : "Format fișier DSN - Fișier cu nume sursă bazei de date",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-ro",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Ce este un fișier DSN?

DSN înseamnă Data Source Name” și este un format de fișier folosit pentru a stoca informații de conexiune la baza de date. Fișierele DSN sunt utilizate în mod obișnuit împreună cu ODBC (Open Database Connectivity) și permit accesul ușor la o anumită bază de date, oferind informațiile necesare pentru a vă conecta la aceasta, cum ar fi numele serverului, numele de utilizator și parola. Fișierul este de obicei în text simplu și poate fi creat și editat folosind un editor de text. Poate fi folosit pe diverse sisteme de operare precum Windows, Linux și Mac.

## Cum se creează un fișier DSN?

Metoda de creare a unui fișier DSN poate varia în funcție de sistemul de operare și de instrumentele disponibile. Următorii pași oferă o prezentare generală a procesului de creare a unui fișier DSN pe un sistem Windows.

1. Deschideți Administratorul sursei de date ODBC căutând Surse de date ODBC” în meniul de pornire.
2. Selectați fila System DSN” și faceți clic pe butonul Add”.
3. Selectați driverul corespunzător pentru baza de date la care doriți să vă conectați și faceți clic pe Finish”.
4. Completați informațiile necesare pentru a vă conecta la baza de date, cum ar fi numele serverului, numele de utilizator și parola.
5. Faceți clic pe OK” pentru a salva fișierul DSN.

Alternativ, puteți crea un fișier DSN manual creând un fișier text simplu cu extensia .dsn și introducând informațiile necesare de conectare în formatul:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Puteți utiliza apoi calea acestui fișier ca DSN în codul/scriptul dumneavoastră pentru a vă conecta la baza de date.

## Programe care deschid fișierul DSN

Un fișier DSN este un fișier text simplu care stochează informații utilizate pentru a se conecta la o bază de date, cum ar fi numele serverului, numele de utilizator și parola. Este de obicei folosit împreună cu ODBC (Open Database Connectivity) pentru a oferi acces ușor la o anumită bază de date.

Pentru a deschide și vizualiza conținutul unui fișier DSN, puteți utiliza orice editor de text, cum ar fi Notepad, Sublime Text, Atom etc. Aceste programe vă vor permite să deschideți fișierul DSN și să vizualizați informațiile de conexiune stocate în acesta.

Cu toate acestea, pentru a utiliza fișierul DSN pentru a vă conecta la o bază de date și a executa operațiuni precum SELECT, INSERT, UPDATE, DELETE etc., un program cu suport ODBC, cum ar fi un limbaj de programare precum Python, Java, C# sau un instrument de gestionare a bazelor de date precum Microsoft Access , este necesar SQL Server Management Studio. Aceste programe pot folosi informațiile din fișierul DSN pentru a se conecta la baza de date și a efectua operația dorită.

## Referințe

* [Ce este un DSN (Numele sursei de date)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



