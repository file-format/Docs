{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB File Format - En Exchange Mail Database File",
  "description":"Läs mer om EDB-filformat och API:er som kan skapa och öppna EDB-filer.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Vad är en EDB fil?

En fil med filtillägget .edb är en postlådedatabas som skapats av Microsoft Exchange Server för att lagra e-postrelaterad data. EDB, Exchange Database, lagrar meddelanden som är pågående och icke-SMTP. EDB är också känd som Extensible Storage Engine (ESE) databasfiler och lagrar filer med b-trädstruktur. Eftersom de är lagringsfiler kan EDB-filer konverteras till andra filformat för e-postlagring såsom [PST](/sv/email/pst/) och [OST](/sv/email/ost/).

## EDB filformat

Det finns inga officiella/öppna EDB-filformatspecifikationer tillgängliga som kan refereras till. Vissa framsteg har gjorts för reverse engineering av filformatet, vilket resulterat i partiell specifikationsavkodning. Enligt dessa består en EDB-fil av:
* Filhuvud - Innehåller information om databasfilhuvud
* Sidor med fast storlek - Innehåller databasen som består av tabeller och index

### Databasfilhuvud
Databasfilens rubrik finns på den första databassidan och är minst 668 byte. Filhuvudet innehåller "Filformatversion" och "Filtyp" förutom andra fält.

#### Filtyper
|Typ|Beskrivning
---|---|
|0| Databas|
|1| Streamar|

`Obs:` Identifierare för dessa typer är inte kända.

#### Filformatversion
Det ursprungliga formatet för EDB startade i april 1997 och fortsatte att utvecklas för förändringar därefter.

|Revisionsdatum|Version|Revision|beskrivning
---|---|---|---|
|april 1997| 0x00000620|0x00000000| Original operativsystem Beta-format.|
|maj 1997 |0x00000620|0x00000001| Lägg till kolumner i katalogen för villkorlig indexering och OLD.|
|Jun 1997|0x00000620|0x00000002|Lägg till flaggan fLocalizedText i IDB.|
|Okt 1997|0x00000620|0x00000003|Lägg till SPLIT_BUFFER för att rymma trädets rotsidor.|
|Jan 1998|0x00000620|0x00000002|Återställ revision för att ESE97 ska förbli framåtkompatibel.|
||0x00000620|0x00000003|Lägg till nya taggade kolumner i katalogen ("CallbackData" och "CallbackDependencies").|
|Maj 1998|0x00000620|0x00000004|Super Long Value (SLV) stöd: signSLV, fSLVEfinns i dbheader.|
|Maj 1998|0x00000620|0x00000005|Nytt SLV-rymdträd.|
|Okt 1998|0x00000620|0x00000006|SLV rymdkarta.|
|Dec 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Jan 1999|0x00000620|0x00000008|Nytt kolumnformat för mall.|
|Jun 1999|0x00000620|0x00000009|Sorterade mallkolumner. Används i Windows XP SP3|
||0x00000620|0x0000000b|Innehåller sidhuvudet med ECC-kontrollsummanUsed in Exchange|
||0x00000620|0x0000000c|Används i Windows Vista (SP0)|
||0x00000620|0x00000011|Stöd för 2 KiB, 16 KiB och 32 KiB sidor.Utökad sidhuvud med ytterligare ECC-kontrollsummor.Kolumnkomprimering.Space-tips.Används i Windows 7 (SP0)|
|maj 1999|0x00000623|0x00000000|Ny rymdhanterare.|

### Databasfiler

EDB-databasfilen innehåller schemat för alla tabeller i databasen. Dessutom innehåller den även poster för alla databastabeller och index för tabellerna. Dess plats bestäms av följande identifierare.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Baserat på dessa kan databasens tillstånd bedömas enligt följande.

|Värde|Identifierare|Beskrivning
---|---|---|
|1|JET_dbstateJustCreated|Databasen skapades precis.|
|2|JET_dbstateDirtyShutdown|Databasen kräver hård eller mjuk återställning för att köras för att bli användbar eller flyttbar. Man bör inte försöka flytta databaser i detta tillstånd.|
|3|JET_dbstateCleanShutdown|Databasen är i rent tillstånd. Databasen kan bifogas utan några loggfiler.|
|4|JET_dbstateBeingConverted|Databasen uppgraderas.|
|5|JET_dbstateForceDetachInternal|Detta värde introduceras i WindowsXP|
 

## Referenser
* [Extensible Storage Engine (ESE) Databas File (EDB) Specifikationer](https://github.com/libyal/libesedb/tree/master/documentation)

