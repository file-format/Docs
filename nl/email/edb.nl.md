{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB-bestandsindeling - een Exchange Mail-databasebestand",
  "description":"Meer informatie over EDB-bestandsindelingen en API's die EDB-bestanden kunnen maken en openen.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Wat is een EDB-bestand?

Een bestand met de bestandsextensie .edb is een mailboxdatabase die is gemaakt door Microsoft Exchange Server om e-mailgerelateerde gegevens op te slaan. EDB, Exchange Database, slaat berichten op die in behandeling zijn en niet-SMTP. EDB staat ook bekend als Extensible Storage Engine (ESE) Database-bestanden en slaat bestanden op met behulp van de b-tree-structuur. Omdat het opslagbestanden zijn, kunnen EDB-bestanden worden geconverteerd naar andere bestandsindelingen voor e-mailopslag, zoals [PST](/nl/email/pst/) en [OST](/nl/email/ost/).

## EDB-bestandsindeling

Er zijn geen officiële/open EDB-specificaties voor bestandsindelingen beschikbaar waarnaar kan worden verwezen. Er is enige vooruitgang geboekt bij het reverse-engineeren van het bestandsformaat, wat heeft geleid tot gedeeltelijke decodering van specificaties. Volgens deze bestaat een EDB-bestand uit:
* Bestandskoptekst - Bevat informatie over de koptekst van het databasebestand
* Pagina's met vaste grootte - Bevat de database die bestaat uit tabellen en indexen

### Database Bestandskop
De header van het databasebestand bevindt zich op de eerste databasepagina en is minimaal 668 bytes. De bestandskop bevat naast andere velden `File Format Version` en `File Type`.

#### Bestand types
|Type|Beschrijving
---|---|
|0| Database|
|1| Streamen|

`Opmerking:` ID's voor deze typen zijn niet bekend.

#### Versie bestandsformaat
Het oorspronkelijke formaat van EDB begon in april 1997 en bleef daarna evolueren voor wijzigingen.

|Revisiedatum|Versie|Revisie|beschrijving
---|---|---|---|
|Apr 1997| 0x00000620|0x00000000| Oorspronkelijke besturingssysteem Beta-formaat.|
|Mei 1997 |0x00000620|0x00000001| Voeg kolommen toe aan de catalogus voor voorwaardelijke indexering en OUD.|
|Jun 1997|0x00000620|0x00000002|Voeg de vlag fLocalizedText toe aan IDB.|
|Oct 1997|0x00000620|0x00000003|Voeg SPLIT_BUFFER toe aan hoofdpagina's van de ruimteboomstructuur.|
|Jan 1998|0x00000620|0x00000002|Revisie terugdraaien zodat ESE97 voorwaarts compatibel blijft.|
||0x00000620|0x00000003|Voeg nieuwe getagde kolommen toe aan de catalogus ("CallbackData" en "CallbackDependencies").|
|Mei 1998|0x00000620|0x00000004|Super Long Value (SLV)-ondersteuning: signSLV, fSLVEbestaat in dbheader.|
|Mei 1998|0x00000620|0x00000005|Nieuwe SLV-ruimteboom.|
|Okt 1998|0x00000620|0x00000006|SLV-ruimtekaart.|
|Dec 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Jan 1999|0x00000620|0x00000008|Nieuwe sjabloonkolomindeling.|
|Jun 1999|0x00000620|0x00000009|Sjabloonkolommen gesorteerd. Gebruikt in Windows XP SP3|
||0x00000620|0x0000000b|Bevat de paginakop met de ECC-checksumUsed in Exchange|
||0x00000620|0x0000000c|Gebruikt in Windows Vista (SP0)|
||0x0000620|0x00000011|Ondersteuning voor 2 KiB-, 16 KiB- en 32 KiB-pagina's. Uitgebreide paginakop met extra ECC-controlesommen. Kolomcompressie. Ruimtehints. Gebruikt in Windows 7 (SP0)|
|Mei 1999|0x00000623|0x00000000|Nieuwe ruimtemanager.|

### Databasebestanden

Het EDB-databasebestand bevat het schema voor alle tabellen in de database. Daarnaast bevat het ook records voor alle databasetabellen en indexen voor de tabellen. De locatie wordt bepaald door de volgende identifiers.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Op basis hiervan kan de staat van de database als volgt worden beoordeeld.

|Waarde|Identificatie|Beschrijving
---|---|---|
|1|JET_dbstateJustCreated|De database is zojuist aangemaakt.|
|2|JET_dbstateDirtyShutdown|De database vereist hard of zacht herstel om bruikbaar of verplaatsbaar te worden. Men moet niet proberen databases in deze staat te verplaatsen.|
|3|JET_dbstateCleanShutdown|De database is in een schone staat. De database kan worden toegevoegd zonder logbestanden.|
|4|JET_dbstateBeingConverted|De database wordt geüpgraded.|
|5|JET_dbstateForceDetachInternal|Deze waarde is geïntroduceerd in WindowsXP|
 

## Referenties
* [Extensible Storage Engine (ESE) Database File (EDB) Specificaties](https://github.com/libyal/libesedb/tree/master/documentation)

