{
  "date": "2020-11-11",
  "keywords": [
"NDF",
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
  "description": "Lær om MDF-filformat og API'er, der kan oprette og åbne NDF-filer.",
  "title": "NDF-filformat - SQL Server-masterdatabasefil",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-daf"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er NDF fil?

En fil med filtypenavnet .ndf er en sekundær databasefil, der bruges af [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) til at gemme brugerdata. NDF er en sekundær lagerfil, fordi SQL-serveren gemmer brugerspecificerede data i den primære lagerfil kendt som [MDF](/database/mdf/). NDF-datafil er valgfri og er brugerdefineret til at administrere datalagring, hvis den primære MDF-fil bruger al den tildelte plads. Det er normalt gemt på separat disk og kan spredes til flere lagerenheder. Tilstedeværelsen af MDF-filer er nødvendig for at åbne NDF-filer.

## NDF filformat

NDF-filformatet er ikke anderledes end [MDF](/database/mdf/) og bruger sider som den grundlæggende enhed for datalagring. hver side starter med 96 bytes overskrift, der inkluderer:

 * Side-id
 * Type af struktur
 * Antal poster på siderne
 * Henvisninger til forrige og næste sider

### NDF-filstruktur

En MDF-fil har følgende datastruktur.

 * Side 0: Overskrift
 * Side 1: Første PFS
 * Side 2: Første GAM
 * Side 3: Første SGAM
 * Side 4: Ubrugt
 * Side 5: Ubrugt
 * Side 6: Første DCM
 * Side 7: Første BCM

#### NDF-filoverskrift

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

## Datafilside

Sider i en SQL Server-datafil starter fra nul (0) og stiger sekventielt. Hver fil genkendes af et unikt fil-id-nummer. Fil-id'et og sidenummerparret identificerer entydigt en side i en database. Et eksempel, der viser sidetal i en database, er som i følgende billede.

{{< figure src="../ndf.png" alt="NDF-databasefilformat" >}}

Dette eksempel viser sidetal i en database, der har en 4 MB primær datafil og 1 MB sekundær datafil.

## Referencer

 * [Databasefiler og filgrupper](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
 * [Database Atach and Attach - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- version 15)
 * [Analyse af SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

