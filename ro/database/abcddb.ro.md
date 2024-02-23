{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aflați despre formatul de fișier ABCDDB și despre API-urile care pot crea și deschide fișiere ABCDDB.",
  "title" : "Format de fișier ABCDDB - Fișier de bază de date din agenda de adrese Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-ro",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Ce este un fișier ABCDDB?

Fișierul cu extensia **.ABCDDB** reprezintă baza de date Apple Address Book Contact List Database. Aparține aplicației **Agendă**, cunoscută și sub denumirea de **Contacte**. Este o aplicație încorporată și inclusă cu sistemele de operare iOS și macOS. Aplicația Contacte permite utilizatorilor să salveze și să organizeze informații legate de contactele lor, inclusiv persoane fizice, companii și organizații. Această aplicație permite utilizatorilor să țină evidența detaliilor precum nume, adrese, numere de telefon și adrese de e-mail, precum și să-și clasifice contactele în grupuri.

## Relația cu SQLite și Calea tipică

Agenda de adrese Apple (cunoscută și sub numele de Contacte) stochează informațiile de contact ca vCards în folderul metadate. **Fișierul _ABCDDB_ este de fapt _SQLite 3 datafile_**.

SQLite este un sistem popular de gestionare a bazelor de date care este conceput pentru a fi ușor și autonom. Este folosit în multe tipuri diferite de software și dispozitive. SQLite este un tip de RDBMS, ceea ce înseamnă că stochează date în tabele care sunt legate între ele prin chei. Poate gestiona o serie de tipuri de date, inclusiv numere întregi, numere în virgulă mobilă, șiruri de caractere și date binare. În plus, SQLite acceptă tranzacții, care le permit utilizatorilor să efectueze mai multe operațiuni de bază de date împreună ca o singură unitate de lucru.

Fișierul cu extensia ABCDDB este de obicei stocat aici

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Remedierea bazei de date de contacte corupte

Vă rugăm mai întâi să faceți backup înainte de a încerca să faceți acest lucru. Apoi, vă rugăm să navigați la

`~/Library/Application Support/AddressBook`

În acel director, veți găsi trei fișiere, inclusiv cel cu extensia .abcddb

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

Ștergeți toate aceste fișiere și redeschideți contactele, va începe să funcționeze din nou.

## Restaurați baza de date AddressBook din Backup

Să presupunem că contactele din baza de date AddressBook sunt stocate în `addressbook-v22.abcddb`

- Mai întâi backup pentru datele din Agendă și închideți toate aplicațiile.
- Mutați fișierul bazei de date în subdirectorul `~/Library/Application Support/AddressBook`
- Lansați **Address Book.app**.

## Exportați datele fișierului ABCDDB în Microsoft Access

Deoarece fișierul este fișierul de date SQLite 3, puteți exporta datele din fișierul abcddb în Microsoft Access folosind conectorul ODBC.

Conectorul SQLite ODBC este o bibliotecă software și un driver care permite aplicațiilor care acceptă interfața ODBC să se conecteze la o bază de date SQLite. Include o bibliotecă care definește interfața ODBC și un driver care traduce această interfață în apeluri către API-ul SQLite. Pentru a utiliza conectorul SQLite ODBC, trebuie mai întâi să îl instalați și apoi să configurați o sursă de date ODBC pe computer. După parcurgerea acestor pași, orice aplicație care este echipată cu suport ODBC se va putea conecta la sursa de date și va putea prelua date din baza de date SQLite.

## Referințe
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Baza de date de contact pentru Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Cum pot deschide sau export un fișier abcddb în Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

