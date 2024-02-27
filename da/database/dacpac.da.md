{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Data Tier AppliCation Package"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DACPAC filformat og API'er, der kan oprette og åbne DACPAC filer.",
  "title": "DACPAC - Data Tier AppliCation Package",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-dac"
}
},
  "lastmod": "2021-09-06"
}

## Hvad er DACPAC fil?

En fil med .dacpac (står for Data Tier AppliCation Package) filtypenavnet er en databasefil, oprettet med Microsoft SQL Server-datalagapplikationen, som indeholder databasemodellen til repræsentation af databaseobjekter. Da den indeholder den komplette model af databasen, bruges den til at gendanne en database fra de detaljer, der er tilgængelige i modellen. DACPAC-filer bliver normalt overdraget til implementeringsteams til installation hos kunden for at gendanne databasen. Disse kan åbnes med
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC-filformat - flere oplysninger

DACPAC-datapakkefilerne er faktisk komprimerede ZIP-filer, der indeholder flere [XML](/web/xml/)-filer, der indeholder information om databasemodellen, såsom tabeller og visninger, der bruges til at gendanne en database. For at se indholdet af DACPAC-filer skal du omdøbe filerne fra .dacpac til [.zip](/compression/zip/) og udpakke zip-arkivet med et hvilket som helst dekomprimeringsværktøj.

Følgende er nogle få filer, der findes i en DACPAC-fil.

 * [Content_Types].xml
```
<?xml version=1.0 encoding=utf-8?>
<Types
xmlns=http://schemas.openxmlformats.org/package/2006/content-types>
<Default Extension=xml ContentType=text/xml />
</Types>
```
 * DacMetadata.xml

```
<?xml version=1.0 encoding=utf-8?>
<DacType xmlns=http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02>
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
 * Origin.xml

 * model.xml

Det skal bemærkes, at DACPAC ikke indeholder DATA og andre objekter på serverniveau. Filen kan indeholde alle objekttyper, som kan opbevares i SSDT-projektet.

## Referencer

* [Data Tier Applications - Benefits](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Deploying a Data Tier Application - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
