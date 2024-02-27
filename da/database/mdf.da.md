{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "Lær om MDF-filformat og API'er, der kan oprette og åbne MDF-filer.",
  "title": "MDF-filformat - SQL Server-masterdatabasefil",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-daf"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er en MDF fil?

En fil med filtypenavnet .mdf er en masterdatabasefil, der bruges af [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) til at gemme brugerdata. Det er af største vigtighed, da alle data er gemt i denne fil. MDF-filen gemmer brugerdata i relationelle databaser i formularkolonner, rækker, felter, indekser, visninger og tabeller. SQL Server gør det muligt at indstille autogrow og autoshrink-indstillinger for at have en positiv indvirkning på databasens ydeevne. MDF-filer kan indlæses og vedhæftes til en database ved hjælp af Microsoft SQL Server. MDF-filer har Application/octet-stream mime-typen.

## MDF filformat

Den grundlæggende enhed for datalagring i SQL Server er en side. En databasetildelt lagerside er opdelt i logiske sider med nummerering fra 0 til n. En enkelt side starter med en overskrift på 96 bytes, der består af side-id, type struktur, siden tilhører, antal poster på siden og pointere til forrige og næste side.

### Filstruktur

En MDF-fil har følgende datastruktur.

 * Side 0: Overskrift
 * Side 1: Første PFS
 * Side 2: Første GAM
 * Side 3: Første SGAM
 * Side 4: Ubrugt
 * Side 5: Ubrugt
 * Side 6: Første DCM
 * Side 7: Første BCM

#### Filoverskrift

Sidenummer 0 i alle filerne indeholder en header, der gemmer metadata om filen.

#### Side ledig plads (PFS)
PFS identificerer allokeringsstatus og bestemmer mængden af ledig plads.

 * Bit 1: Angiver om siden er allokeret eller ej.
 * Bit 2: Angiver om siden er fra en blandet udstrækning.
 * Bit 3: Indikerer, at denne side er en IAM-side.
 * Bit 4: Indikerer, at denne side indeholder spøgelsesposter
 * Bit 5 til 7: En kombineret tre-bit værdi, som angiver sidefylden som følger:
   * 0: Siden er tom
   * 1: Siden er 1–50 % fuld
   * 2: Siden er 51–80 % fuld
   * 3: Siden er 81–95 % fuld
   * 4: Siden er 96–100 % fuld

## Referencer

 * [Databasefiler og filgrupper](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Database Atach and Attach - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- version 15)
 * [Analyse af SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

