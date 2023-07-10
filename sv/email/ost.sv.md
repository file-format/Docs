{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook Storage File Format",
  "description":"Läs mer om OST-filformat och API:er som kan skapa och öppna OST-filer.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en OST fil?

OST eller offlinelagringsfiler representerar användarens postlådedata i offlineläge på lokal dator vid registrering med Exchange Server med Microsoft Outlook. Den skapas automatiskt vid första användningen av Microsoft Outlook vid anslutning till servern. När filen väl har skapats synkroniseras data med e-postservern så att den är tillgänglig offline även i händelse av frånkoppling från e-postservern. OST-filer kan använda postlådeobjekt som e-post, kontakter, kalenderinformation, anteckningar, uppgifter och annan liknande data. Användare kan skapa e-postmeddelanden och andra dataobjekt i OST-fil även i avsaknad av anslutning till servern, men dessa kommer inte att synkroniseras med servern. När anslutningen är upprättad synkroniseras den lokala filen med servern igen så att både servern och den lokala kopian är på samma informationsnivå.

## OST filformat

Filformaten OST (Offline Storage Table) och [PST](/sv/email/pst/) (Personal Storage Table) består av formatet Personal Folder File (PFF) som motsvarar lagring av användarens e-postmeddelanden, kontakter och möten. Data i en PFF-fil lagras i little-endian med alla datum och tider representerade som FILETIME i UTC. [MS-PST] definierar två typer av PFF:

* 32-bitars ANSI-format
* 64-bitars Unicode-format

PST-filformat [specifikationer](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), som är tillgängligt från Microsoft, är också tillämpliga på OST-filformat som gratis och oåterkallelig patentlicensering genom Open Specification Promise. Den består av följande särskiljbara element:

* Fle header
* Filhuvuddata
* Index grennod
* Indexbladsnod
* (Fil) offset index
* (Artikel) deskriptorindex
* Lokala beskrivningar
* Typ av objekttabell

### Rubrikinformation

HEADER-strukturen för OST-filen finns i början av filen vid 0 offset. Den innehåller metadatainformation om OST-filen och ROOT-informationen för att komma åt NDB Layer-datastrukturerna som beskrivs ovan. HEADER-strukturen skiljer sig för Unicode- och ANSI-versionerna av OST-filformat.

Rubriken börjar med ett 4-byte magiskt ord **!BDN** representerat av byte (0x21, 0x42, 0x44, 0x4E). Ett annat 2-byte magiskt nummer, **SM** (0x53, 0x4D), finns vid offset 8 från början av filen. Versionsinformation (ANSI eller Unicode) ligger på en offset på 10 från början av filen. Hexvärde (0x17) anger Unicode OST-fil medan 0x0E eller 0x0F representerar ANSI-filformat.

|Fält|Beskrivning
---|---|
|dwMagic (4 byte)|MÅSTE vara "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 byte)|32-bitars CRC-värdet för de 471 byten med data från wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|MÅSTE vara "{ 0x53, 0x4D }".
|wVer (2 byte)|Filformatversion. Detta värde MÅSTE vara 14 eller 15 om filen är en ANSI PST-fil och MÅSTE vara 23 om filen är en Unicode PST-fil.
|wVerClient (2 byte)|Version av klientfilformat. Den version som motsvarar formatet som beskrivs i detta dokument är 19. Skapare av en ny PST-fil baserad på detta dokument BÖR initialisera detta värde till 19.
|bPlatformCreate (1 byte)|Detta värde MÅSTE sättas till 0x01.
|bPlatformAccess (1 byte)|Detta värde MÅSTE sättas till 0x01.
|dwReserved (8 byte)|
|bidUnused (endast 8 byte Unicode)|Oanvänd utfyllnad lades till när Unicode PST-filformatet skapades.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|Nästa sida BID. Sidor har en speciell räknare för att tilldela bidIndex-värden. Värdet på bidIndex för BID för sidor tilldelas från denna räknare.
|bidNextB (endast 4 byte ANSI): |Next BID. Detta värde är den monotona räknaren som indikerar det BID som ska tilldelas för nästa allokerade block. BID-värden ökar i steg om 4. För mer information, se avsnitt 2.2.2.2.
|dwUnique (4 bytes)|Detta är ett monotont ökande värde som ändras varje gång PST-filens HEADER-struktur ändras. Funktionen för detta värde är att tillhandahålla ett unikt värde och att säkerställa att HEADERS CRC:erna är olika efter varje rubrikändring.
|rgnid[](128 byte)|En fast array med 32 NID, var och en motsvarar en av de 32 möjliga NID_TYPE:erna (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_MESSAGE)_ASS_MESSAGE)
|qwUnused (8 byte)|Oanvänt utrymme; MÅSTE sättas till noll. Endast Unicode PST-filformat.
|root (Unicode: 72 byte; ANSI: 40 byte)|En ROOT-struktur (avsnitt 2.2.2.5).
|dwAlign (4 byte)|Oanvända justeringsbyte; MÅSTE sättas till noll. Endast Unicode PST-filformat.
|rgbFM (128 byte)|Utfasad FMap. Detta används inte längre och MÅSTE fyllas med 0xFF. Läsare BÖR ignorera värdet på dessa bytes.
|rgbFP (128 byte)|Utfasad FPMap. Detta används inte längre och MÅSTE fyllas med 0xFF. Läsare BÖR ignorera värdet på dessa bytes.
|bSentinel (1 byte)|MÅSTE ställas in på 0x80.
|bCryptMethod (1 byte)|Indikerar hur data i PST-filen är kodad. MÅSTE ställas in på ett av de fördefinierade värdena (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved (2 byte)| Reserverad; MÅSTE sättas till noll.
|bidNextB (8 byte)|Indikerar nästa tillgängliga BID-värde. Endast Unicode PST-filformat.
|bidNextB (ENDAST Unicode: 8 byte)|Nästa BID. Detta värde är den monotona räknaren som indikerar det BID som ska tilldelas för nästa allokerade block. BID-värden ökar i steg om 4. För mer information, se avsnitt 2.2.2.2.
|dwCRCFull (4 bytes)|32-bitars CRC-värdet för de 516 byten med data från wMagicClient till och med bidNextB. Endast Unicode PST-filformat.
|ullReserved (8 byte)|Reserved; MÅSTE sättas till noll. Endast ANSI PST-filformat.
|dwReserved (4 byte)|Reserverad; MÅSTE sättas till noll. Endast ANSI PST-filformat.
|rgbReserved2 (3 byte)|
|bReserverad (1 byte) |
|rgbReserved3 (32 byte) |

## Referenser

* [Outlook Personal Folders (.ost) Filformat](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

