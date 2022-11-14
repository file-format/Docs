{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote-bestandsindeling",
  "description":"Meer informatie over EEN bestandsindeling en API's die EEN bestanden kunnen maken en openen.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een .ONE-bestand? ##

Bestand vertegenwoordigd door de extensie .ONE wordt gemaakt door de Microsoft OneNote-toepassing. Met OneNote kunt u informatie verzamelen met de toepassing alsof u uw conceptblok gebruikt om aantekeningen te maken. OneNote-bestanden kunnen verschillende elementen bevatten die op niet-vaste locaties op documentpagina's kunnen worden geplaatst. Deze elementen kunnen tekst, gedigitaliseerd handschrift en objecten bevatten die zijn gekopieerd uit andere toepassingen, waaronder afbeeldingen, tekeningen en multimedia (audio/video) clips. Microsoft biedt nu een online versie van OneNote aan als onderdeel van Office365, waar Notes via internet kan worden gedeeld met andere OneNote-gebruikers.

## .ONE bestandsformaat specificaties ##

De OneNote-bestandsindeling biedt een effectieve manier om digitale notities weer te geven als hiërarchische sets van secties en pagina's. Elke pagina bevat door de gebruiker gedefinieerde inhoud in een specifieke structuur voor weergave door het bestandsformaat Document Object Model (DOM). Het datamodel voor dit formaat is zoals hieronder geïllustreerd.

### Structuuroverzicht ###

Zoals geïllustreerd in het gegevensmodel voor OneNote-bestandsindeling, bestaat een OneNote-document uit verschillende elementen.

#### Sectie ####

Een sectie is de bovenste container in een OneNote-bestand dat verder verschillende elementen bevat, zoals:

* Pagina's
* Metagegevens
* Eigendommen

Metagegevens en eigenschappen omvatten de sectienaam, identificatie van de pagina's die in de sectie zijn opgenomen en de volgorde waarin die pagina's verschijnen. De term "sectie" verwijst naar alle pagina's in een sectie en de weergave van die gegevens in een OneNote®-revisiebestand met de bestandsnaamextensie .one.

#### Bladzijde ####

Door de gebruiker gedefinieerde inhoud in een OneNote-document bevindt zich op een pagina. Pagina-informatie omvat tekst, lijsten, tabellen, paginatitels, afbeeldingen en notitietags. Een pagina bestaat uit omtrekobjecten waaraan de meeste van de ingesloten objecten zijn toegevoegd. Elke pagina kan een naam krijgen voor een betekenisvolle weergave en objecten kunnen ook direct aan pagina's worden toegevoegd. Een pagina kan verder subpagina's bevatten in een hiërarchisch systeem.

#### Eigenschappen en eigenschappensets ####

De inhoud van OneNote bestaat uit eigenschappen, eigenschappensets en bestandsgegevensobjecten. Een eigenschappenset is een verzameling eigenschappen die een bepaald type inhoud vertegenwoordigt. Een bestandsgegevensobject is een blok binaire gegevens dat afbeeldingen, ingesloten bestanden of audio-/video-inhoud bevat.

#### OneNote-notitieblok ####

Een notebook is een verzameling sectiebestanden die in dezelfde map zijn opgeslagen. Een verzameling eigenschappen wordt gebruikt om instellingen op te geven, zoals de volgorde van de secties in het notitieblok en de kleur van het notitieblok.

### Bestandsstructuur ###

Een revisiearchiefbestand MOET beginnen met een **Header**-structuur. De rest van het bestand is opgedeeld in blokken van bytes, waarbij de grootte en structuur van elk blok wordt gespecificeerd door het veld dat ernaar verwijst. Een blok is bereikbaar als ernaar wordt verwezen door de **Header**-structuur, of als ernaar wordt verwezen door een veld in een ander bereikbaar blok. Gegevens buiten de **Header**-structuur en alle bereikbare blokken MOETEN worden genegeerd.

Alle structuren zijn uitgelijnd op 1-byte grenzen. Alle gehele getallen zijn ondertekend, tenzij anders aangegeven. Alle velden zijn [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), tenzij anders aangegeven.

#### Koptekst ####

De header van het .ONE-bestand bestaat uit stukjes die verschillende unieke id's en velden bevatten voor de weergave van bestandsinformatie als volgt:

`guidFileType (16 bytes):` Een GUID die het type van het revisieopslagbestand specificeert. MOET een van de waarden uit de volgende tabel zijn.


|Bestandsindeling|Waarde
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Een GUID die de identiteit van dit revisie-archiefbestand specificeert. MOET wereldwijd uniek zijn.

`guidLegacyFileVersion (16 bytes):` MOET "{00000000-0000-0000-0000-000000000000}" zijn en MOET worden genegeerd.

`guidFileFormat (16 bytes):` Een GUID die aangeeft dat het bestand een revisie-archiefbestand is. MOET "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}" zijn.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Een niet-ondertekend geheel getal. MOET een van de waarden in de volgende tabel zijn, afhankelijk van het bestandstype.

|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Een niet-ondertekend geheel getal. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.


|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Een niet-ondertekend geheel getal. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.

|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Een geheel getal zonder teken. MOET een van de waarden in de volgende tabel zijn, afhankelijk van de bestandsindeling van dit bestand.

|Bestandsindeling|Waarde
--- | --- |
|.een|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Een **FileChunkReference32**-structuur die de waarde "fcrZero" MOET hebben.

`fcrLegacyTransactionLog (8 bytes):` Een **FileChunkReference32**-structuur die "fcrNil" MOET zijn.

`cTransactionsInLog (4 bytes):` Een geheel getal zonder teken dat het aantal transacties in het transactielogboek aangeeft. MOET NIET nul zijn.

`cbLegacyExpectedFileLength (4 bytes):` Een geheel getal zonder teken dat nul MOET zijn en MOET worden genegeerd.

`rgbPlaceholder (8 bytes):` Een geheel getal zonder teken dat nul MOET zijn en MOET worden genegeerd.

`fcrLegacyFileNodeListRoot (8 bytes):` Een **FileChunkReference32**-structuur die "fcrNil" MOET zijn.

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Een geheel getal zonder teken dat nul MOET zijn en MOET worden genegeerd.

`fNeedsDefrag (1 byte):` MOET worden genegeerd.

`fRepairedFile (1 byte):` MOET worden genegeerd.

`fNeedsGabageCollect (1 byte):` MOET worden genegeerd.

`fHasNoEmbeddedFileObjects (1 byte):` Een geheel getal zonder teken dat nul MOET zijn en MOET worden genegeerd.

`guidAncestor (16 bytes):` Een GUID die het veld **Header.guidFile** van het inhoudsopgavebestand specificeert, gegeven door de volgende tabel:


|Inhoudsopgave bestandsformaat|Locatie van inhoudsopgave bestand
--- | --- |
|Section File - .One|Inhoudsopgave bestand bevindt zich in dezelfde directory als dit bestand.
|Inhoudsopgave-bestand - .onetoc2|Inhoudsopgave-bestand bevindt zich in de bovenliggende map van dit bestand.

Als de GUID {00000000-0000-0000-0000-000000000000} is, verwijst dit veld niet naar een inhoudsopgavebestand.

`crcName (4 bytes):` Een niet-ondertekend geheel getal dat de CRC-waarde aangeeft van de naam van dit revisie-archiefbestand. De naam is de Unicode-weergave van de bestandsnaam met de extensie en een extra null-teken aan het einde. Deze CRC wordt altijd berekend met behulp van het CRC-algoritme voor het .one-bestand, ongeacht deze bestandsindeling voor revisieopslag.

`fcrHashedChunkList (12 bytes):` Een **FileChunkReference64x32** structuur die een verwijzing specificeert naar de eerste **FileNodeListFragment** in een gehashte chunklijst. Als de waarde van de **FileChunkReference64x32**-structuur "fcrZero" of "fcrNil" is, bestaat de gehashte chunk-lijst niet.

`fcrTransactionLog (12 bytes):` Een **FileChunkReference64x32**-structuur die een verwijzing specificeert naar de eerste **TransactionLogFragment**-structuur in een transactielogboek. De waarde van het veld **fcrTransactionLog** MOET NIET "fcrZero" zijn en MAG NIET "fcrNil" zijn.

`fcrFileNodeListRoot (12 bytes):` Een **FileChunkReference64x32**-structuur die een verwijzing naar een lijst met rootbestandsknooppunten specificeert. De waarde van het veld **fcrFileNodeListRoot** MOET NIET "fcrZero" zijn en MAG NIET "fcrNil" zijn.

`fcrFreeChunkList (12 bytes):` Een **FileChunkReference64x32** structuur die een verwijzing specificeert naar de eerste **FreeChunkListFragment** structuur. Als de waarde van de **FileChunkReference64x32**-structuur "fcrZero" of "fcrNil" is, bestaat de lijst met gratis chunks niet.

`cbExpectedFileLength (8 bytes):` Een niet-ondertekend geheel getal dat de grootte, in bytes, van dit revisiearchiefbestand aangeeft.

`cbFreeSpaceInFreeChunkList (8 bytes):` Een geheel getal zonder teken dat de grootte, in bytes, MOET specificeren van de vrije ruimte gespecificeerd door de lijst met vrije chunks.

`guidFileVersion (16 bytes):` Een GUID. Wanneer de waarde van het veld **cTransactionsInLog** of het veld **guidDenyReadFileVersion** wordt gewijzigd, MOET **guidFileVersion** worden gewijzigd in een nieuwe GUID.

`nFileVersionGeneration (8 bytes):` Een niet-ondertekend geheel getal dat aangeeft hoe vaak het bestand is gewijzigd. MOET worden verhoogd wanneer het veld **guidFileVersion** verandert.

`guidDenyReadFileVersion (16 bytes):` Een GUID. Wanneer de bestaande inhoud van het bestand wordt gewijzigd, met uitzondering van de **Header**-structuur van het bestand en ongebruikte opslagblokken, MOET **guidDenyReadFileVersion** worden gewijzigd in een nieuwe GUID.

`grfDebugLogFlags (4 bytes):` MOET nul zijn. MOET worden genegeerd.

`fcrDebugLog (12 bytes):` Een **FileChunkReference64x32** structuur die de waarde "fcrZero" MOET hebben. MOET worden genegeerd.

`fcrAllocVerificationFreeChunkList (12 bytes):` Een **FileChunkReference64x32** structuur die "fcrZero" MOET zijn. MOET worden genegeerd.

`bnCreated (4 bytes):` Een niet-ondertekend geheel getal dat het buildnummer aangeeft van de toepassing die dit revisiebestand heeft gemaakt. MOET worden genegeerd.

`bnLastWroteToThisFile (4 bytes):` Een niet-ondertekend geheel getal dat het buildnummer aangeeft van de toepassing die het laatst naar dit revisiebestand heeft geschreven. MOET worden genegeerd.

`bnOldestWritten (4 bytes):` Een niet-ondertekend geheel getal dat het buildnummer aangeeft van de oudste toepassing die naar dit revisiebestand heeft geschreven. MOET worden genegeerd.

`bnNewestWritten (4 bytes):` Een niet-ondertekend geheel getal dat het buildnummer aangeeft van de nieuwste toepassing die naar dit revisiebestand heeft geschreven. MOET worden genegeerd.

`rgbReserved (728 bytes):` MOET nul zijn. MOET worden genegeerd.

## Referenties ##

* [[MS-ONESTORE] - OneNote-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

