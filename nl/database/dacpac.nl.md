{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Data Tier-toepassingspakket"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DACPAC-bestandsindelingen en API's die DACPAC-bestanden kunnen maken en openen.",
  "title" :"DACPAC - Data Tier-toepassingspakket",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Wat is een DACPAC-bestand?

Een bestand met de extensie .dacpac (staat voor Data Tier AppliCation Package) is een databasebestand, gemaakt met de Microsoft SQL Server-gegevenslaagtoepassing, dat het databasemodel bevat voor de weergave van databaseobjecten. Omdat het het volledige model van de database bevat, wordt het gebruikt om een database te herstellen op basis van de details die in het model beschikbaar zijn. DACPAC-bestanden worden meestal overgedragen aan implementatieteams voor installatie bij de klant om de database te herstellen. Deze kunnen worden geopend met
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019)

## DACPAC-bestandsindeling - Meer informatie

De DACPAC-gegevenspakketbestanden zijn eigenlijk gecomprimeerde ZIP-bestanden die verschillende [XML](/nl/web/xml/)-bestanden bevatten met informatie over het databasemodel, zoals tabellen en weergaven, die worden gebruikt om een database te herstellen. Om de inhoud van DACPAC-bestanden te bekijken, hernoemt u de bestanden van .dacpac naar [.zip](/nl/compression/zip/) en extraheert u het zip-archief met een decompressieprogramma.

Hieronder volgen enkele bestanden die te vinden zijn in een DACPAC-bestand.

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
* Oorsprong.xml

* model.xml

Opgemerkt moet worden dat DACPAC geen DATA en andere objecten op serverniveau bevat. Het bestand kan alle objecttypen bevatten die in het SSDT-project kunnen worden bewaard.

## Referenties

* [Data Tier Applications - Voordelen](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Een Data Tier-applicatie implementeren - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Hoe maak je een DACPAC-bestand aan?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

