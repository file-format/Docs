{
  "date": "2020-11-11",
  "keywords": [
"MDB",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MDB failu formātu un API, kas var izveidot un atvērt MDB failus.",
  "title": "MDB faila formāts — Microsoft Access datu bāzes fails",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-lvb"
}
},
  "lastmod": "2020-11-11"
}

## Kas ir MDB fails?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. Microsoft Access sānu versijās tiek izmantoti [ACCDB](/database/accdb/) failu formāti, kas ir līdz šim jaunākais faila formāts. MDB failus var atvērt ar tādām lietojumprogrammām kā Microsoft Access, MDB Viewer, MDBOpener, un tos var pārvērst ACCDB, [CSV](/spreadsheet/csv/), Excel formātos utt.

## MDB faila formāts

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Lapas

Saskaņā ar neoficiālo MDB rokasgrāmatu MDB fails sastāv no fiksēta izmēra lapām (2048 baiti Jeb DB3 un 4096 baiti Jet DB 4). Pirmais baits norāda lapas veidu. Tālāk ir norādīti galvenie lapu veidi.

Pirmā lapa: tajā ir ietverta datu bāzes galvenes informācija, kas ietver arī tās Jet DB versijas identifikāciju, ar kuru fails ir saderīgs. Turklāt tajā ir iekļauta arī failu drošības informācija un lapas lietojuma karte.

`Tabulas definīciju lapa:` Tabulas definīciju lapa norāda kolonnas, datu tipus, indeksu un citu informāciju. Ja nepieciešams, tajā tiek izmantotas papildu lapas, un tajā ir iekļauta lapu karte, kurā ir šīs tabulas rindu dati.

Datu lapas: datu lapas ir faktiskie datu konteineri, kuros dati tiek glabāti pa rindām. Tas izmanto papildu lapas, lai saglabātu garas datu vērtības.

Viena Microsoft Access datu bāze var sastāvēt no vairākiem failiem, kas ļauj pārsniegt failu un tabulu lieluma ierobežojumus. Tas atvieglo veidlapu un koda ievietošanu priekšgala MDB failā uz lietotāja darbvirsmas un datu ievietošanu citos MDB aizmugures failos serveros, kas savienoti ar tīklu.

## Atsauces Nr.

* [Piekļuves specifikācijas](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Neoficiālā MDB rokasgrāmata] (http://jabakobob.net/mdb/)


