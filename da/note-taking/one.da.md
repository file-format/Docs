{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONE - Microsoft OneNote-filformat",
  "description": "Lær om ONE filformat og API'er, der kan oprette og åbne ONE filer.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-dae"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en .ONE fil? ##

Filer repræsenteret af .ONE-udvidelsen er oprettet af Microsoft OneNote-applikationen. OneNote lader dig indsamle oplysninger ved hjælp af applikationen, som om du bruger din kladdeblok til at tage noter. OneNote-filer kan indeholde forskellige elementer, der kan placeres på ikke-faste placeringer på dokumentsider. Disse elementer kan indeholde tekst, digitaliseret håndskrift og objekter kopieret fra andre applikationer, herunder billeder, tegninger og multimedieklip (lyd/video). Microsoft tilbyder nu onlineversion af OneNote som en del af Office365, hvor noter kan deles med andre OneNote-brugere over internettet.

## .ONE Filformatspecifikationer ##

OneNote-filformatet giver en effektiv måde at repræsentere digitale noter som hierarkiske sæt af sektioner og sider. Hver side indeholder brugerdefineret indhold i en specifik struktur til repræsentation ved filformatet Document Object Model (DOM). Datamodellen for dette format er som illustreret nedenfor.

### Strukturoversigt ###

Som illustreret i datamodellen for OneNote-filformatet, består et OneNote-dokument af forskellige elementer.

#### Afsnit ####

En sektion er den øverste container i en OneNote-fil, der yderligere indeholder forskellige elementer i den som:

* Sider

* Metadata

* Ejendomme


Metadata og egenskaber omfatter sektionsnavnet, identifikation af de sider, der er indeholdt i sektionen, og den rækkefølge, som disse sider vises i. Udtrykket sektion refererer til alle de sider, der er i en sektion, og repræsentationen af disse data i en OneNote® revisionsbutiksfil, som har filtypenavnet .one.

#### Side ####

Brugerdefineret indhold i et OneNote-dokument er indeholdt på en side. Sideoplysninger omfatter tekst, lister, tabeller, sidetitler, billeder og notemærker. En side består af konturobjekter, hvortil de fleste af de indeholdte objekter er tilføjet. Hver side kan tildeles et navn for meningsfuld repræsentation, og objekter kan også tilføjes direkte til siderne. En side kan yderligere indeholde undersider i et hierarkisk system.

#### Egenskaber og egenskabssæt ####

OneNote-indhold består af egenskaber, egenskabssæt og fildataobjekter. Et egenskabssæt er en samling af egenskaber, der repræsenterer en eller anden type indhold. Et fildataobjekt er en blok af binære data, der indeholder billeder, indlejrede filer eller lyd-/videoindhold.

#### OneNote Notebook ####

En notesbog er en samling af sektionsfiler, der er gemt i samme mappe. En samling af egenskaber bruges til at angive indstillinger såsom rækkefølgen af sektionerne i notesbogen og farven på notesbogen.

### Filstruktur ###

En revisionslagerfil SKAL begynde med en **Header**-struktur. Resten af filen er opdelt i blokke af bytes, hvor størrelsen og strukturen af hver blok er specificeret af feltet, der refererer til den. En blok er tilgængelig, hvis den refereres af **Header**-strukturen, eller hvis den refereres af et felt i en anden tilgængelig blok. Data uden for **Header**-strukturen og alle tilgængelige blokke SKAL ignoreres.

Alle strukturer er justeret på 1-byte grænser. Alle heltal er signerede, medmindre andet er angivet. Alle felter er [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), medmindre andet er angivet.

#### Header ####

Headeren af .ONE-filen består af bidder, der indeholder forskellige unikke id'er og felter til repræsentation af filoplysninger som følger:

`guidFileType (16 bytes):` En GUID, der specificerer typen af revisionslagerfilen. SKAL være en af værdierne fra følgende tabel.


|Filformat|Værdi
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` En GUID, der specificerer identiteten af denne revisionslagerfil. SKAL være globalt unikt.

`guidLegacyFileVersion (16 bytes):` SKAL være {00000000-0000-0000-0000-000000000000} og SKAL ignoreres.

`guidFileFormat (16 bytes):` En GUID, der angiver, at filen er en revisionsbutiksfil. SKAL være {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filtypen.

|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHaswrittenToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.


|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.

|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.

|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` En **FileChunkReference32** struktur, der SKAL have værdien fcrZero.

`fcrLegacyTransactionLog (8 bytes):` En **FileChunkReference32** struktur, der SKAL være fcrNil.

`cTransactionsInLog (4 bytes):` Et heltal uden fortegn, der angiver antallet af transaktioner i transaktionsloggen. MÅ IKKE være nul.

`cbLegacyExpectedFileLength (4 bytes):` Et heltal uden fortegn, der SKAL være nul og SKAL ignoreres.

`rgbPlaceholder (8 bytes):` Et heltal uden fortegn, der SKAL være nul og SKAL ignoreres.

`fcrLegacyFileNodeListRoot (8 bytes):` En **FileChunkReference32** struktur, der SKAL være fcrNil.

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Et heltal uden fortegn, der SKAL være nul og SKAL ignoreres.

`fNeedsDefrag (1 byte):` SKAL ignoreres.

`fRepairedFile (1 byte):` SKAL ignoreres.

`fNeedsGarbageCollect (1 byte):` SKAL ignoreres.

`fHasNoEmbeddedFileObjects (1 byte):` Et heltal uden fortegn, der SKAL være nul og SKAL ignoreres.

`guidAncestor (16 bytes):` En GUID, der specificerer feltet **Header.guidFile** i indholdsfortegnelsesfilen, givet af følgende tabel:


|Indholdsfortegnelse Filformat|Placering af Indholdsfortegnelse Fil
--- | --- |
|Section File - .One|Indholdsfortegnelsesfil er placeret i samme mappe som denne fil.
|Indholdsfortegnelsesfil - .onetoc2|Indholdsfortegnelsesfil er placeret i denne fils overordnede mappe.

Hvis GUID'et er {00000000-0000-0000-0000-000000000000}, refererer dette felt ikke til en indholdsfortegnelsesfil.

`crcName (4 bytes):` Et usigneret heltal, der specificerer CRC-værdien af navnet på denne revisionslagerfil. Navnet er Unicode-repræsentationen af filnavnet med dets udvidelse og et ekstra nul-tegn i slutningen. Denne CRC beregnes altid ved hjælp af CRC-algoritmen for .one-filen, uanset dette revisionslagerfilformat.

`fcrHashedChunkList (12 bytes):` En **FileChunkReference64x32** struktur, der specificerer en reference til det første **FileNodeListFragment** i en hashed chunkliste. Hvis værdien af **FileChunkReference64x32**-strukturen er fcrZero eller fcrNil, eksisterer den hasherede chunk-liste ikke.

`fcrTransactionLog (12 bytes):` En **FileChunkReference64x32**-struktur, der specificerer en reference til den første **TransactionLogFragment**-struktur i en transaktionslog. Værdien af feltet **fcrTransactionLog** MÅ IKKE være fcrZero og MÅ IKKE være fcrNil.

`fcrFileNodeListRoot (12 bytes):` En **FileChunkReference64x32** struktur, der specificerer en reference til en rodfil nodeliste. Værdien af feltet **fcrFileNodeListRoot** MÅ IKKE være fcrZero og MÅ IKKE være fcrNil.

`fcrFreeChunkList (12 bytes):` En **FileChunkReference64x32** struktur, der specificerer en reference til den første **FreeChunkListFragment** struktur. Hvis værdien af **FileChunkReference64x32** strukturen er fcrZero eller fcrNil, så eksisterer den frie chunkliste ikke.

`cbExpectedFileLength (8 bytes):` Et heltal uden fortegn, der angiver størrelsen, i bytes, af denne revisionslagerfil.

`cbFreeSpaceInFreeChunkList (8 bytes):` Et heltal uden fortegn, der SKAL angive størrelsen, i bytes, af den ledige plads, der er angivet af listen over frie stykker.

`guidFileVersion (16 bytes):` En GUID. Når enten værdien af feltet **cTransactionsInLog** eller feltet **guidDenyReadFileVersion** ændres, SKAL **guidFileVersion** ændres til en ny GUID.

`nFileVersionGeneration (8 bytes):` Et heltal uden fortegn, der angiver antallet af gange, filen har ændret sig. SKAL øges, når feltet **guidFileVersion** ændres.

`guidDenyReadFileVersion (16 bytes):` En GUID. Når det eksisterende indhold af filen ændres, undtagen **Header**-strukturen af filen og ubrugte lagerblokke, SKAL **guidDenyReadFileVersion** ændres til en ny GUID.

`grfDebugLogFlags (4 bytes):` SKAL være nul. SKAL ignoreres.

`fcrDebugLog (12 bytes):` En **FileChunkReference64x32** struktur, der SKAL have en værdi fcrZero. SKAL ignoreres.

`fcrAllocVerificationFreeChunkList (12 bytes):` En **FileChunkReference64x32** struktur, der SKAL være fcrZero. SKAL ignoreres.

`bnCreated (4 bytes):` Et heltal uden fortegn, der specificerer build-nummeret for den applikation, der oprettede denne revisionslagerfil. BØR ignoreres.

`bnLastWroteToThisFile (4 bytes):` Et usigneret heltal, der specificerer build-nummeret for den applikation, der sidst skrev til denne revisionslagerfil. BØR ignoreres.

`bnOldestWritten (4 bytes):` Et usigneret heltal, der specificerer build-nummeret for den ældste applikation, der skrev til denne revisionslagerfil. BØR ignoreres.

`bnNewestWritten (4 bytes):` Et usigneret heltal, der specificerer build-nummeret for den nyeste applikation, der skrev til denne revisionslagerfil. BØR ignoreres.

`rgbReserved (728 bytes):` SKAL være nul. SKAL ignoreres.

## Referencer ##

* [[MS-ONESTORE] - OneNote-filformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


