{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR File - dBASE Structure List Object File - Ce este fișierul .str și cum se deschide?",
  "description" : "Aflați despre STR dBASE Structure List Object File și despre cum să îl deschideți.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-ro",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Ce este un fișier STR?

Formatul de fișier STR este asociat în mod obișnuit cu dBASE, un sistem de gestionare a bazelor de date. În dBASE, un fișier .str reprezintă de obicei un fișier obiect listă de structură. Acest fișier conține structura unui tabel de bază de date, inclusiv informații despre câmpuri (coloane) și proprietățile acestora.

Fișierul obiect listă de structură (.str) conține metadate cum ar fi numele câmpurilor, tipurile de date, lungimile câmpurilor și orice alte proprietăți asociate fiecărui câmp din tabelul bazei de date. Este folosit pentru a defini structura tabelului bazei de date fără a conține înregistrări de date reale.

Programe precum dBASE sau alte instrumente de gestionare a bazelor de date pot utiliza acest fișier pentru a înțelege aspectul tabelului bazei de date și pentru a efectua operațiuni precum interogarea, actualizarea sau crearea de noi înregistrări pe baza acestei structuri.

Iată un exemplu de bază despre ceea ce poate conține un fișier STR:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Acest exemplu descrie un tabel cu patru câmpuri: ID, Nume, Vârstă și Data de naștere, împreună cu tipurile și lungimile de date respective.

## Cum se deschide fișierul STR?

Principala modalitate de a deschide fișierele .str este utilizarea dBASE în sine, în special pe sistemele de operare Windows. dBASE este capabil să citească și să interpreteze conținutul acestor fișiere, permițând utilizatorilor să vizualizeze și să lucreze cu structura bazei de date.

Deoarece fișierele .str sunt în esență fișiere text simplu care conțin informații despre structura bazei de date, le puteți deschide și folosind un editor de text. Exemple de editori de text includ Microsoft Notepad pe Windows și Apple TextEdit pe Mac. Când este deschis într-un editor de text, veți putea vedea conținutul fișierului, inclusiv numele câmpurilor, tipurile de date și alte informații structurale, într-un format care poate fi citit de om.

## Referințe
* [dBase](https://en.wikipedia.org/wiki/DBase)


