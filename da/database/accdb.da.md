{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
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
  "description": "Lær om ACCDB filformat og API'er, der kan oprette og åbne ACCDB filer.",
  "title": "ACCDB-filformat - Microsoft Access 2007-databasefil",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-dab"
}
},
  "lastmod": "2020-11-12"
}

## Hvad er en ACCDB fil?

En fil med filtypen .accdb er en Microsoft Access 2007-databasefil, der gemmer brugerdata i tabeller. Det understøtter opbevaring
tilpassede formularer, SQL-forespørgsler og andre data. ACCDB-filer erstattede [MDB](/database/mdb/)-filer, efter at Microsoft skiftede til XML-baseret filstruktur. ACCDB-filer kan stadig konverteres til MDB med gammel kompatibilitet. Imidlertid er ACCDB det meget brugte Access-databasefilformat nu. Microsoft understøttede også yderligere funktioner i ACCDB-format, såsom mulighed for at gemme vedhæftede filer, binære data og understøttelse af flere værdier.

## ACCDB filformat

Ligesom MDB er der ingen offentlige specifikationer tilgængelige for ACCDB-filformat. Microsoft understøtter adgang til disse filer programmæssigt via Open Database Connectivity (ODBC) standard og Visual Basic for Applications (VBA).

### En indsigt

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. I ACCDB-filer ser denne indikator ud til at afspejle kompatibiliteten af filen snarere end versionen af ACE-motoren, der blev brugt til at oprette den.

## Referencer

* [Access 2016 Specifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Hvilket Access-filformat skal jeg bruge?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


