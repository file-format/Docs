{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Datanivåapplikationspaket" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DACPAC-filformat och API:er som kan skapa och öppna DACPAC-filer.",
  "title" :"DACPAC - Data Tier Application Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Vad är en DACPAC fil?

En fil med tillägget .dacpac (står för Data Tier AppliCation Package) är en databasfil, skapad med Microsoft SQL Server-applikationen för datanivåer, som innehåller databasmodellen för representation av databasobjekt. Eftersom den innehåller hela modellen av databasen, används den för att återställa en databas från den information som finns tillgänglig i modellen. DACPAC-filer överlämnas vanligtvis till distributionsteam för installation i kundens lokaler för att återställa databasen. Dessa kan öppnas med
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC-filformat - Mer information

DACPAC-datapaketfilerna är faktiskt komprimerade ZIP-filer som innehåller flera [XML](/sv/web/xml/)-filer som innehåller information om databasmodellen, såsom tabeller och vyer, som används för att återställa en databas. För att se innehållet i DACPAC-filer, byt namn på filerna från .dacpac till [.zip](/sv/compression/zip/) och extrahera zip-arkivet med valfritt dekompressionsverktyg.

Följande är några filer som finns i en DACPAC-fil.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* model.xml

Det bör noteras att DACPAC inte innehåller DATA och andra objekt på servernivå. Filen kan innehålla alla objekttyper som kan finnas kvar i SSDT-projektet.

## Referenser

* [Data Tier Applications - Benefits](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Deploying a Data Tier Application - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Hur skapar man DACPAC-fil?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

