{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PST - Outlook Personal Information Store-filformat",
  "description": "Lær om PST-filformat og API'er, der kan oprette og åbne PST-filer.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ps-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PST fil?

Filer med filtypenavnet .pst repræsenterer Outlook Personal Storage Files (også kaldet Personal Storage Table), der gemmer forskellige brugeroplysninger. Brugeroplysninger gemmes i mapper af forskellige typer, der inkluderer e-mails, kalenderelementer, noter, kontakter og flere andre filformater. PST-filer bruges til at arkivere e-mail-data offline, som senere kan indlæses og ses i forskellige applikationer.

## PST-filformatspecifikationer

PST-filformatet [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) er tilgængelige fra Microsoft som gratis og uigenkaldelig gratis patentlicens gennem Open Specification Promise.

### Type af PST-formater

PST-filformater er kategoriseret i to typer baseret på kodningen af filtypen. ANSI-kodede PST-filer er ældre filformater og understøttes kun af Outlook 2002 og tidligere versioner. Sådanne filer har en maksimal størrelsesgrænse på 2 GB (2^^31^^ Bytes) og understøtter ikke Unicode. En mere moderne filformattype, baseret på Unicode-kodning, fjerner filstørrelsesbegrænsningen og kan nå en maksimal datastørrelse på 50 GB.

### Logisk organisering af PST-filformat

I bunden af PST-filformatet ligger B-Tree, der holder data sorteret og tillader søgninger, sekventiel adgang, indsættelser, sletninger osv. i logaritmisk tid. Den overordnede struktur af en PST-fil er organiseret i tre lag.

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - Nodedatabaselag ligger på det lavere niveau af en PST-fil og inkluderer en database med noder. Disse noder repræsenterer faktisk lavere lagerfaciliteter i PST-filformatet. NDB-laget består af header, filallokeringsoplysninger, blokke og BTrees (Node BTree og Block BTree) fra lagringssynspunkt. Noder og blokke af NDB-lag er forbundet via Data BID, som er en af de fire egenskaber ved Node reference, dvs. NID (Node ID), Parent NID, Data BID (Block BID) og SubNode BID.

`Lists, Tables and Properties Layer -` LTP-laget giver den logiske forståelse af begreber på højere niveau oven på NDB. Udover andre elementer består LTP-laget hovedsageligt af Property Context (PC) og Table Context (TC). PC er en samling af egenskaber, mens TC repræsenterer en todimensionel matrix af samling af egenskaber vs. tilstedeværelsen af disse. Effektiv implementering af pc'er og TC'er, LTP-laget bruger følgende to typer datastrukturer på toppen af NDB-knuden:

* Heap On Node (HN) - gør det muligt at underallokere datastrømmen fra en node i små fragmenter af variabel størrelse.

* BTree on Heap (BTH) - BTH giver en bekvem og praktisk måde at søge gennem data-pc'er, beskrevet ovenfor, er implementeret som BTH'er, og det er derfor, det implementeres ved at bygge inde i en HN-struktur.


`Messaging Layer -` Regler på højere niveau og forretningslogik til at arbejde med PST-filer er implementeret på dette lag. Det logiske output af dette lag resulterer som mappeobjekter, meddelelsesobjekter, vedhæftede objekter og egenskaber, hvilket er gjort muligt ved at kombinere LTP- og NDB-lag. Regler og krav, som skal følges ved ændring af PST-indholdet, er også defineret på dette lag.

### Fysisk organisering af PST-filformat

Højt niveau af filorganisering af PST-fil er som vist i figuren nedenfor. Dette er blot en oversigt over forskellige koncepter fra logiske elementer i PST-fil.

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST Header Information

HEADER-strukturen af PST-filen er placeret i begyndelsen af filen ved 0 offset. Den indeholder metadataoplysninger om PST-filen og ROOT-oplysningerne for at få adgang til NDB Layer-datastrukturerne beskrevet ovenfor. HEADER-strukturen er forskellig for Unicode- og ANSI-versionerne af PST-filformatet.

Overskriften starter med et 4-bytes magisk ord **!BDN** repræsenteret af bytes (0x21, 0x42, 0x44, 0x4E). Et andet 2-bytes magisk tal, **SM** (0x53, 0x4D), er placeret ved offset 8 fra starten af filen. Versionsoplysninger (ANSI eller Unicode) ligger med en offset på 10 fra starten af filen. Hex-værdi (0x17) angiver Unicode PST-fil, mens 0x0E eller 0x0F repræsenterer ANSI-filformat.

|Felt|Beskrivelse
---|---|
|dwMagic (4 bytes)|SKAL være { 0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 bytes)|32-bit CRC-værdien af de 471 bytes data startende fra wMagicClient (0ffset 0x0008)
|wMagicClient (2 bytes)|SKAL være { 0x53, 0x4D }.
|wVer (2 bytes)|Filformatversion. Denne værdi SKAL være 14 eller 15, hvis filen er en ANSI PST-fil, og SKAL være 23, hvis filen er en Unicode PST-fil.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Skabere af en ny PST-fil baseret på dette dokument BØR initialisere denne værdi til 19.
|bPlatformCreate (1 byte)|Denne værdi SKAL sættes til 0x01.
|bPlatformAccess (1 byte)|Denne værdi SKAL sættes til 0x01.
|dwReserved (8 bytes)|
|bidUnused (kun 8 bytes Unicode)|Ubrugt udfyldning tilføjet, da Unicode PST-filformatet blev oprettet.
|bidNextP (Unicode: 8 bytes; ANSI: 4 bytes)|Næste side BID. Sider har en speciel tæller til tildeling af bidIndex-værdier. Værdien af bidIndex for BID'er for sider tildeles fra denne tæller.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. For flere detaljer, se afsnit 2.2.2.2.
|dwUnique (4 bytes)|Dette er en monotont stigende værdi, der ændres hver gang PST-filens HEADER-struktur ændres. Funktionen af denne værdi er at give en unik værdi og at sikre, at HEADER CRC'erne er forskellige efter hver overskriftsændring.
|rgnid[] (128 bytes)|En fast matrix af 32 NID'er, der hver svarer til en af de 32 mulige NID_TYPE'er (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_NORMAL_MESSAGE,NID_MESSAGE)
|qwUnused (8 bytes)|Ubrugt plads; SKAL sættes til nul. Kun Unicode PST-filformat.
|root (Unicode: 72 bytes; ANSI: 40 bytes)|En ROOT-struktur (afsnit 2.2.2.5).
|dwAlign (4 bytes)|Ubrugte justeringsbytes; SKAL sættes til nul. Kun Unicode PST-filformat.
|rgbFM (128 bytes)|Udgået FMap. Denne bruges ikke længere og SKAL udfyldes med 0xFF. Læsere BØR ignorere værdien af disse bytes.
|rgbFP (128 bytes)|Udgået FPMap. Denne bruges ikke længere og SKAL udfyldes med 0xFF. Læsere BØR ignorere værdien af disse bytes.
|bSentinel (1 byte)|SKAL indstilles til 0x80.
|bCryptMethod (1 byte)|Angiver, hvordan dataene i PST-filen er kodet. SKAL indstilles til en af de foruddefinerede værdier (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserveret (2 bytes)| reserveret; SKAL sættes til nul.
|bidNextB (8 bytes)|Indikerer den næste tilgængelige BID-værdi. Kun Unicode PST-filformat.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. For flere detaljer, se afsnit 2.2.2.2.
|dwCRCFull (4 bytes)|32-bit CRC-værdien af de 516 bytes data, der starter fra wMagicClient til og med bidNextB. Kun Unicode PST-filformat.
|ullReserved (8 bytes)|Reserveret; SKAL sættes til nul. Kun ANSI PST filformat.
|dwReserved (4 bytes)|Reserveret; SKAL sættes til nul. Kun ANSI PST filformat.
|rgbReserved2 (3 bytes)|
|bReserveret (1 byte) |
|rgbReserved3 (32 bytes) |

### Data beskyttelse ###

Af sikkerhedsmæssige årsager kan PST-filer også beskyttes med adgangskode, hvilket kræver, at indlæsningsapplikationen anvender adgangskode, før den kan ses. Adgangskoden anvendt til PST-filen gemmes i beskedlageret. Dette giver dog ikke stærk databeskyttelse, da adgangskoden kan fjernes med tilgængelige værktøjer. Desuden bruges brugerspecificeret adgangskode ikke som en del af nøglen til kodning og afkodning af chifferalgoritmer. Der er således ingen fordel ved at beskytte data, der skal tilgås af uautoriserede parter. Lagring af adgangskode som CRC-32-hash af den originale streng gør det også til en svag metode til datasikkerhed mod brute-force-tilgang.

## Referencer ##

* [Outlook Personal Folders (.pst) filformat](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


