{
  "date" : "2019-12-09",
  "keywords" :[ "zip-fil", "zip-filformat", "vad är en zip-fil", "fil", "zip-exempel", "zip-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BLIXTLÅS",
  "description":"Vad är en ZIP-fil och API:er som kan skapa och öppna ZIP-filer.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Vad är en ZIP-fil? ##

En fil med filtillägget .zip är ett arkiv som kan innehålla en eller flera filer eller kataloger. Arkivet kan ha komprimering tillämpad på de inkluderade filerna för att minska ZIP-filstorleken. ZIP-filformat offentliggjordes redan i februari 1989 av Phil Katz för att uppnå arkivering av filer och mappar. Formatet gjordes till en del av verktyget [PKZIP](https://www.pkware.com/pkzip), skapat av PKWARE, Inc. Direkt efter att [tillgängliga specifikationer](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), gjorde många företag ZIP-filformat till en del av sina programvaruverktyg, inklusive Microsoft (sedan Windows 7), Apple (Mac OS X) och många andra.

## Kort historik över ZIP-filformat

Historiken för ZIP-filformat går tillbaka till händelsen av en rättsprocess som System Enhancement Associates (SEA) riktade mot PKWARE för att ha använt dess ARC-verktyg utan tillstånd för dess varumärke och upphovsrätten till produktens utseende och användargränssnitt. Innan detta hade Phil Katz skrivit om SEA:s källkod och släppt PKXARC, en ARC-extraktor, och PKARC, en filkompressor, som gratisprogram för MS-DOS-baserade system. Förlorade i rättegången, PKWARE kunde inte längre använda något som var relaterat till ARC. Det var här skapandet av en ny filkomprimering kom till, kallad ZIP som gjordes till en del av PKZIP-verktyget hos PKWARE, Inc.

Katz släppte ZIP-filformatspecifikationerna till det offentliga, samtidigt som de behöll äganderätten till sitt komprimerings- och extraheringsverktyg, dvs. PKZIP. ZIP-komprimeringssystemet kunde (och kan) arkivera filer i en mapp med hjälp av en 32-bitars cyklisk redundanskontroll ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritm för att komprimera fil storlekar. Till skillnad från ARC inkluderade .ZIP-mappar en katalogfil som spelade rollen som en kryptografs kodbok, som innehöll den information som krävs för att rendera de komprimerade filerna.

## Komprimeringsmetoder som stöds i ZIP

Enligt specifikationer för .ZIP-filformat stöds följande komprimeringsmetoder.

* Store - innebär ingen komprimering
* Krympa
* Reduktion (Detta innebär kompressionsfaktorer som sträcker sig från nivå 1 till nivå 4)
* Implodera
*Tömma luften
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd version I, Rev 1

DEFLATE är den vanligaste komprimeringsmetoden som är en förlustfri datumkomprimeringsalgoritm som använder en kombination av LZ77 och Huffman-kodning och som beskrivs i [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specifikationer för ZIP-filformat

ZIP-filer har kapacitet att lagra flera filer med olika komprimeringstekniker samtidigt som de stöder lagring av en fil utan någon komprimering. Varje fil lagras/komprimeras individuellt vilket hjälper till att extrahera dem, eller lägga till nya, utan att komprimera eller dekomprimera hela arkivet.

### Övergripande ZIP-filformat

Varje zip-fil är strukturerad på följande sätt:


|ZIP-filformat
---|
|Lokal filhuvud 1
|Fildata 1
|Databeskrivning 1
| Lokal filhuvud 2
|Fildata 2
|Databeskrivning 2
| ....
| ....
|Lokal filhuvud N
|Fildata N
|Databeskrivning N
|Arkivdekrypteringshuvud
|Arkiv extra datapost
|Central katalog

ZIP-filformatet använder 32-bitars CRC-algoritm för arkiveringsändamål. För att rendera de komprimerade filerna, har ett ZIP-arkiv en katalog i slutet som håller posten för de inneslutna filerna och deras plats i arkivfilen. Den spelar således rollen som kodning för att kapsla in information som är nödvändig för att rendera de komprimerade filerna. ZIP-läsare använder katalogen för att ladda listan med filer utan att läsa hela ZIP-arkivet. Formatet behåller dubbla kopior av katalogstrukturen för att ge bättre skydd mot förlust av data.

Varje fil i ett ZIP-arkiv representeras som en individuell post där varje post består av en lokal filhuvud följt av den komprimerade fildatan. Katalogen i slutet av arkivet innehåller referenserna till alla dessa filposter. ZIP-filläsare bör undvika att läsa de lokala filhuvudena och alla typer av fillistor bör läsas från katalogen. Denna katalog är den enda källan för giltiga filposter i arkivet eftersom filer kan läggas till mot slutet av arkivet också. Det är därför om en läsare läser lokala rubriker i ett ZIP-arkiv från början, kan den läsa ogiltiga (borttagna) poster liksom de som inte är en del av katalogen som tas bort från arkivet.

Ordningen på filposterna i den centrala katalogen behöver inte sammanfalla med ordningen på filposterna i arkivet.

### ZIP-filposter

Posterna i ZIP-filen är ordnade efter varandra där varje post består av:

* Lokal filhuvud
* Valfria extra datafält
* Användardata (valfritt komprimerad/valfritt krypterad)

Den lokala filhuvudet för varje post representerar information om filen såsom kommentar, filstorlek och filnamn. De extra datafälten (valfritt) kan rymma information för utökningsalternativ för ZIP-formatet.

#### Lokal filhuvud

Den lokala filhuvudet har en specifik fältstruktur som består av flerbytevärden. Alla värden lagras i little-endian byteordning där fältlängden räknar längden i byte. Alla strukturer i en ZIP-fil använder 4-byte signaturer för varje filpost. Slutet på den centrala katalogsignaturen är 0x06054b50 och kan särskiljas med sin egen unika signatur. Följande är ordningen för information som lagras i lokal filhuvud.


|Offset|Byte|Beskrivning
---|---|---|
|0|4|Lokal filhuvudsignatur # 0x04034b50 (läs som ett litet-endiannummer)
|4|2|Version som behövs för att extrahera (minst)
|6|2|Bitflagga för allmänt ändamål
|8|2|Kompressionsmetod
|10|2|Fil senaste ändringstid
|12|2|Fil senaste ändringsdatum
|14|4|CRC-32
|18|4|Komprimerad storlek
|22|4|Okomprimerad storlek
|26|2|Filnamnets längd (n)
|28|2|Extra fältlängd (m)
|30|n|Filnamn
|30+n|m|Extra fält

#### Central Directory File Header


|Offset|Byte|Beskrivning
---|---|---|
|0|4|Central katalogfilhuvudsignatur # 0x02014b50
|4|2|Version gjord av
|6|2|Version som behövs för att extrahera (minst)
|8|2|Bitflagga för allmänt ändamål
|10|2|Kompressionsmetod
|12|2|Fil senaste ändringstid
|14|2|Fil senaste ändringsdatum
|16|4|CRC-32
|20|4|Komprimerad storlek
|24|4|Okomprimerad storlek
|28|2|Filnamnets längd (n)
|30|2|Extra fältlängd (m)
|32|2|Längd på filkommentar (k)
|34|2|Disknummer där filen startar
|36|2|Interna filattribut
|38|4|Externa filattribut
|42|4|Relativ förskjutning av lokal filhuvud. Detta är antalet byte mellan starten av den första disken där filen förekommer och starten av den lokala filhuvudet. Detta tillåter programvara som läser den centrala katalogen för att lokalisera filens position i ZIP-filen.
|46|n|Filnamn
|46+n|m|Extra fält
|46+n+m|k|Filkommentar

#### Slut på centralkatalogpost


|Offset|Byte|Beskrivning
---|---|---|
|0|4|Slut på central katalogsignatur # 0x06054b50
|4|2|Nummer på denna disk
|6|2|Disk där den centrala katalogen startar
|8|2|Antal centrala katalogposter på denna disk
|10|2|Totalt antal centrala katalogposter
|12|4|Storlek på central katalog (byte)
|16|4|Förskjutning av start av central katalog, relativt start av arkiv
|20|2|Kommentarlängd (n)
|22|n|Kommentar

## Referenser

* [PKWARE ZIP-filformatspecifikationer](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Structure of PKZip File](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
