{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST - Outlook Storage File Format",
  "description": "Lær om OST-filformat og API'er, der kan oprette og åbne OST-filer.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en OST fil?

OST eller Offline Storage Files repræsenterer brugerens postkassedata i offlinetilstand på lokal maskine ved registrering med Exchange Server ved hjælp af Microsoft Outlook. Den oprettes automatisk ved første brug af Microsoft Outlook ved forbindelse med serveren. Når filen er oprettet, synkroniseres dataene med e-mail-serveren, så de er tilgængelige offline også i tilfælde af afbrydelse af e-mail-serveren. OST-filer kan bruge postkasseelementer såsom e-mails, kontakter, kalenderoplysninger, noter, opgaver og andre lignende data. Brugere kan oprette e-mails og andre dataelementer i OST-fil, selv i mangel af forbindelse til serveren, men disse vil ikke blive synkroniseret med serveren. Når forbindelsen er etableret, synkroniseres den lokale fil med serveren igen, så både serveren og den lokale kopi er på samme informationsniveau.

## OST filformat

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32-bit ANSI-format

* 64-bit Unicode-format


PST-filformatet [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), som tilgængeligt fra Microsoft, gælder også for OST-filformatet som gratis og uigenkaldelig patentlicens gennem Open Specification Promise. Den består af følgende elementer, der kan skelnes:

* Fle header

* Filoverskriftsdata

* Indeks gren node

* Indeksbladsknudepunkt

* (Fil) offset indeks

* (Vare) deskriptorindeks

* Lokale beskrivelser

* Varetabeltype


### Overskriftsoplysninger

OST-filens HEADER-struktur er placeret i begyndelsen af filen ved 0 offset. Den indeholder metadataoplysninger om OST-filen og ROOT-oplysningerne for at få adgang til NDB Layer-datastrukturerne beskrevet ovenfor. HEADER-strukturen er forskellig for Unicode- og ANSI-versionerne af OST-filformatet.

Overskriften starter med et 4-bytes magisk ord **!BDN** repræsenteret af bytes (0x21, 0x42, 0x44, 0x4E). Et andet 2-bytes magisk tal, **SM** (0x53, 0x4D), er placeret ved offset 8 fra starten af filen. Versionsoplysninger (ANSI eller Unicode) ligger med en offset på 10 fra starten af filen. Hex-værdi (0x17) angiver Unicode OST-fil, mens 0x0E eller 0x0F repræsenterer ANSI-filformat.

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

## Referencer

* [Outlook personlige mapper (.ost) filformat](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


