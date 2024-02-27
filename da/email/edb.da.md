{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EDB-filformat - En Exchange Mail-databasefil",
  "description": "Lær om EDB-filformat og API'er, der kan oprette og åbne EDB-filer.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-dab"
}
},
  "lastmod": "2020-09-16"
}

## Hvad er en EDB fil?

En fil med filtypenavnet .edb er en postkassedatabase oprettet af Microsoft Exchange Server til at gemme mailrelaterede data. EDB, Exchange Database, gemmer meddelelser, der er i gang og ikke-SMTP. EDB er også kendt som Extensible Storage Engine (ESE)-databasefiler og lagerfiler ved hjælp af b-træstruktur. Da de er lagringsfiler, kan EDB-filer konverteres til andre e-mail-lagringsfilformater såsom [PST](/email/pst/) og [OST](/email/ost/).

## EDB filformat

Der er ingen officielle/åbne EDB-filformatspecifikationer tilgængelige, der kan refereres til. Der er gjort nogle fremskridt for reverse engineering af filformatet, hvilket resulterer i delvis specifikationsafkodning. Ifølge disse består en EDB-fil af:
 * File Header - Indeholder oplysninger om databasefilheader
 * Sider med fast størrelse - Indeholder databasen, der består af tabeller og indekser

### Databasefiloverskrift
Databasefilens header findes på den første databaseside og er på mindst 668 bytes. Filoverskriften indeholder `Filformatversion` og `Filtype` ud over andre felter.

#### Filtyper
|Type|Beskrivelse
---|---|
|0| Database|
|1| Streaming|

`Bemærk:` Identifikatorer for disse typer kendes ikke.

#### Filformatversion
Det oprindelige format af EDB startede i april 1997 og fortsatte med at udvikle sig til ændringer derefter.

|Revsion Date|Version|Revision|description
---|---|---|---|
|april 1997| 0x00000620|0x00000000| Originalt operativsystem Beta-format.|
|Maj 1997 |0x00000620|0x00000001| Tilføj kolonner i kataloget til betinget indeksering og OLD.|
|Jun 1997|0x00000620|0x00000002|Tilføj flaget fLocalizedText i IDB.|
|Okt 1997|0x00000620|0x00000003|Tilføj SPLIT_BUFFER til mellemrumstræets rodsider.|
|Jan 1998|0x00000620|0x00000002|Tilbagefør revision for at ESE97 forbliver fremadkompatibel.|
||0x00000620|0x00000003|Tilføj nye mærkede kolonner til kataloget (CallbackData og CallbackDependencies).|
|Maj 1998|0x00000620|0x00000004|Super Long Value (SLV) support: signSLV, fSLVEeksisterer i dbheader.|
|Maj 1998|0x00000620|0x00000005|Nyt SLV-rumtræ.|
|Okt. 1998|0x00000620|0x00000006|SLV-rumkort.|
|Dec 1998|0x00000620|0x00000007|4-byte IDXSEG.|
|Jan 1999|0x00000620|0x00000008|Nyt skabelon kolonneformat.|
|Jun 1999|0x00000620|0x00000009|Sorterede skabelonkolonner. Brugt i Windows XP SP3|
||0x00000620|0x0000000b|Indeholder sidehovedet med ECC checksumUsed in Exchange|
||0x00000620|0x0000000c|Brugt i Windows Vista (SP0)|
||0x00000620|0x00000011|Understøttelse af 2 KiB, 16 KiB og 32 KiB sider.Udvidet sidehoved med yderligere ECC-kontrolsummer.Kolonnekomprimering.Space-tip.Bruges i Windows 7 (SP0)|
|Maj 1999|0x00000623|0x00000000|Ny Space Manager.|

### Databasefiler

EDB-databasefilen indeholder skemaet for alle tabellerne i databasen. Derudover inkluderer det også poster for alle databasetabeller og indekser for tabellerne. Dens placering bestemmes af følgende identifikatorer.

* JetCreateDatabase

* JetCreateDatabase2

* JetAttachDatabase

* JetAttachDatabase2


Baseret på disse kan databasens tilstand vurderes som følger.

|Værdi|Identifier|Beskrivelse
---|---|---|
|1|JET_dbstateJustCreated|Databasen er lige oprettet.|
|2|JET_dbstateDirtyShutdown|Databasen kræver hård eller blød gendannelse for at blive kørt for at blive brugbar eller flytbar. Man bør ikke forsøge at flytte databaser i denne tilstand.|
|3|JET_dbstateCleanShutdown|Databasen er i en ren tilstand. Databasen kan vedhæftes uden logfiler.|
|4|JET_dbstateBeingConverted|Databasen er ved at blive opgraderet.|
|5|JET_dbstateForceDetachInternal|Denne værdi er introduceret i WindowsXP|
 
## Referencer
 * [Extensible Storage Engine (ESE) Database File (EDB) Specifikationer](https://github.com/libyal/libesedb/tree/main/documentation)

