{
  "date": "2020-11-11",
  "keywords": [
"MDB",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MDB failo formatą ir API, kurios gali kurti ir atidaryti MDB failus.",
  "title": "MDB failo formatas – „Microsoft Access“ duomenų bazės failas",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-ltb"
}
},
  "lastmod": "2020-11-11"
}

## Kas yra MDB failas?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. Šoninėse Microsoft Access versijose naudojami [ACCDB](/database/accdb/) failų formatai, kurie yra naujausias iki šiol failo formatas. MDB failus galima atidaryti naudojant tokias programas kaip Microsoft Access, MDB Viewer, MDBOpener ir konvertuoti į ACCDB, [CSV](/spreadsheet/csv/), Excel formatus ir kt.

## MDB failo formatas

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Puslapiai

Kaip nurodyta neoficialiame MDB vadove, MDB failą sudaro fiksuoto dydžio puslapiai (2048 baitai Jeb DB3 ir 4096 baitai Jet DB 4). Pirmasis baitas nurodo puslapio tipą. Toliau pateikiami pagrindiniai puslapių tipai:

Pirmasis puslapis: jame yra duomenų bazės antraštės informacija, kuri taip pat apima Jet DB versijos, su kuria failas yra suderinamas, identifikavimą. Be to, jame taip pat yra failų saugos informacija ir puslapio naudojimo žemėlapis.

Lentelės apibrėžimo puslapis: lentelės apibrėžimo puslapis nurodo stulpelius, duomenų tipus, rodyklę ir kitą informaciją. Jei reikia, naudojami papildomi puslapiai ir pateikiamas puslapių žemėlapis, kuriame yra šios lentelės eilutės duomenys.

Duomenų puslapiai: duomenų puslapiai yra faktiniai duomenų konteineriai, kuriuose duomenys saugomi eilutėmis. Jis naudoja papildomus puslapius ilgoms duomenų reikšmėms saugoti.

Vieną Microsoft Access duomenų bazę gali sudaryti keli failai, leidžiantys viršyti failų ir lentelių dydžio apribojimus. Tai palengvina formų ir kodų įdėjimą į vartotojo darbalaukio MDB failą ir duomenis į kitus MDB failus, esančius prie tinklo prijungtuose serveriuose.

## Nuorodos Nr.
* [Prieigos specifikacijos](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

