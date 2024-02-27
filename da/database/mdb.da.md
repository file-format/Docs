{
  "date": "2020-11-11",
  "keywords": [
"MDB",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MDB-filformat og API'er, der kan oprette og åbne MDB-filer.",
  "title": "MDB-filformat - En Microsoft Access-databasefil",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-dab"
}
},
  "lastmod": "2020-11-11"
}

## Hvad er en MDB fil?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. De laterale versioner af Microsoft Access bruger filformaterne [ACCDB](/database/accdb/), som er det seneste filformat til dato. MDB-filer kan åbnes med applikationer som Microsoft Access, MDB Viewer, MDBOpener og kan konverteres til ACCDB, [CSV](/spreadsheet/csv/), Excel-formater osv.

## MDB filformat

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Sider

Ifølge den uofficielle MDB-vejledning består en MDB-fil af sider med fast størrelse (2048 bytes for Jeb DB3 og 4096 bytes for Jet DB 4). Den første byte angiver sidetypen. Følgende er de vigtigste sidetyper:

`Første side:` Den indeholder oplysninger om databaseheader, der også omfatter identifikation af den Jet DB-version, som filen er kompatibel med. Derudover inkluderer det også filsikkerhedsoplysninger og et kort over sidebrug.

`Tabeldefinitionsside:` En tabeldefinitionsside angiver kolonner, datatyper, indeks og andre oplysninger. Den bruger yderligere sider, hvis det kræves, og inkluderer et kort over sider, der indeholder rækkedata for denne tabel.

`Datasider:` Datasiderne er de faktiske databeholdere, hvor data gemmes i rækker. Den bruger underordnede sider til at gemme lange dataværdier.

En enkelt Microsoft Access-database kan bestå af flere filer, der gør det muligt at overskride fil- og tabelstørrelsesbegrænsninger. Dette letter at lægge formularer og kode i en frontend MDB-fil på brugerens skrivebord og data i en anden backend MDB-filer på servere, der er tilsluttet netværket.

## Referencer ##

* [Adgangsspecifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Den uofficielle MDB-vejledning](http://jabakobob.net/mdb/)


