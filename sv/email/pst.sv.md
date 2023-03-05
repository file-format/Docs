{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Personal Information Store File Format",
  "description":"Läs mer om PST-filformat och API:er som kan skapa och öppna PST-filer.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PST-fil?

Filer med tillägget .pst representerar Outlook Personal Storage Files (även kallad Personal Storage Table) som lagrar olika användarinformation. Användarinformation lagras i mappar av olika typer som inkluderar e-postmeddelanden, kalenderobjekt, anteckningar, kontakter och flera andra filformat. PST-filer används för att arkivera e-postdata offline som senare kan laddas och visas i olika applikationer.

## PST-filformatspecifikationer

PST-filformat [specifikationer](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) är tillgängliga från Microsoft som gratis och oåterkallelig fri patentlicens genom Open Specification Promise .

### Typ av PST-format

PST-filformat är kategoriserade i två typer baserat på kodningen av filtypen. ANSI-kodade PST-filer är äldre filformat och stöds endast av Outlook 2002 och tidigare versioner. Sådana filer har en maximal storleksgräns på 2 GB (2^^31^^ byte) och stöder inte Unicode. En modernare filformatstyp, baserad på Unicode-kodning, tar bort filstorleksbegränsningen och kan nå en maximal datastorlek på 50 GB.

### Logisk organisation av PST-filformat

I basen av PST-filformatet ligger B-Tree som håller data sorterad och tillåter sökningar, sekventiell åtkomst, infogning, radering etc. i logaritmisk tid. Den övergripande strukturen för en PST-fil är organiserad i tre lager.

![Logical layers of a PST file](/sv/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - Noddatabaslager ligger på den lägre nivån av en PST-fil och inkluderar en databas med noder. Dessa noder representerar faktiskt lägre lagringsmöjligheter i PST-filformatet. NDB-skiktet består av header, filallokeringsinformation, block och BTrees (Node BTree och Block BTree) från lagringssynpunkt. Noder och block av NDB-skikt är länkade via Data BID som är en av de fyra egenskaperna för nodreferens, dvs. NID (Nod ID), Parent NID, Data BID (Block BID) och SubNode BID.

`Lists, Tables and Properties Layer -` LTP-lager ger den logiska förståelsen av begrepp på högre nivå ovanpå NDB. Förutom andra element består LTP-lagret huvudsakligen av egenskapskontext (PC) och tabellkontext (TC). PC är en samling egenskaper, medan TC representerar en tvådimensionell matris av samling av egenskaper kontra förekomsten av dessa. Effektiv implementering av datorer och TC:er, LTP-lagret använder följande två typer av datastrukturer ovanpå NDB-noden:

* Heap On Node (HN) - möjliggör underallokering av dataströmmen från en nod i små fragment av variabel storlek.
* BTree on Heap (BTH) - BTH tillhandahåller ett bekvämt och praktiskt sätt att söka igenom data-datorer, som beskrivs ovan, är implementerade som BTH:er och det är därför det implementeras genom att bygga inuti en HN-struktur.

`Meddelandelager -` Regler på högre nivå och affärslogik för att arbeta med PST-filer är implementerade i detta lager. Den logiska utmatningen av detta lager resulterar som mappobjekt, meddelandeobjekt, bilagaobjekt och egenskaper, vilket görs möjligt genom att kombinera LTP- och NDB-lager. Regler och krav, som måste följas vid ändring av PST-innehållet, definieras också i detta lager.

### Fysisk organisation av PST-filformat

Hög nivå av filorganisation för PST-fil är som visas i figuren nedan. Detta är bara en översikt över olika koncept från logiska delar av PST-filen.

![Physical organization of the PST file format](/sv/email/PST-2.png "Physical organization of the PST file format")


#### PST Header Information

HEADER-strukturen för PST-filen finns i början av filen med 0 offset. Den innehåller metadatainformation om PST-filen och ROOT-informationen för att komma åt NDB Layer-datastrukturerna som beskrivs ovan. HEADER-strukturen skiljer sig för Unicode- och ANSI-versionerna av PST-filformatet.

Rubriken börjar med ett 4-byte magiskt ord **!BDN** representerat av byte (0x21, 0x42, 0x44, 0x4E). Ett annat 2-byte magiskt nummer, **SM** (0x53, 0x4D), finns vid offset 8 från början av filen. Versionsinformation (ANSI eller Unicode) ligger på en offset på 10 från början av filen. Hexvärde (0x17) anger Unicode PST-fil medan 0x0E eller 0x0F representerar ANSI-filformat.

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
|rgnid[](128 bytes)|En fast array med 32 NID, var och en motsvarande en av de 32 möjliga NID_TYPE:erna (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_MESSAGE)_ASS_MESSAGE)
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

### Dataskydd ###

För säkerhets skull kan PST-filer också vara lösenordsskyddade, vilket kräver att laddningsapplikationen tillämpar ett lösenord innan det kan visas. Lösenordet som tillämpas på PST-filen lagras i meddelandearkivet. Detta ger dock inget starkt dataskydd eftersom lösenordet kan tas bort med tillgängliga verktyg. Användarspecificerat lösenord används inte heller som en del av nyckeln för kodning och avkodning av chifferalgoritmer. Det finns alltså ingen fördel med att skydda data som kan kommas åt av obehöriga parter. Lagring av lösenord som CRC-32-hash av den ursprungliga strängen gör det också till en svag metod för datasäkerhet mot brute-force-metoden.

## Referenser ##

* [Outlook Personal Folders (.pst) filformat](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

