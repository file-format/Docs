{
  "date": "2019-10-11",
  "keywords": [
"tga fil",
"tga filformat",
"hvad er en tga fil",
"fil",
"tga eksempel",
"tga filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGA-filformat - En TARGA-grafisk billedfil",
  "description": "Lær om TGA-filformat og API'er, der kan oprette og åbne TGA-filer.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-daa"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en TGA fil?

En fil med filtypenavnet .tga er et rastergrafikformat og blev skabt af Truevision Inc. Den blev designet til TARGA-kortene (Truevision Advanced Raster Adapter) og gav understøttelse af Highcolor/truecolor-skærme til IBM-kompatible pc'er. Den understøtter 8, 16, 24 og 32 bits pr. pixel og 8-bit alfakanal. Det understøtter også tabsfri RLE-komprimering, der kan anvendes til at reducere billedstørrelsen. Digitale fotos og teksturer bruger TGA-billedformatet.

## Kort historie

Dannelse af TGA-filformat blev til i 1984 af AT&T EPICenter (senere udvundet og dannet som en uafhængig enhed kendt som Truevision), der arbejdede på markedsføring af nye teknologier udviklet af AT&T til farverammebuffere. EPICenter arbejdede allerede på sine første to kort, VDA (Video Display Adapter) og ICB (image capture board), hvor arbejde på to filtyper, .vda og .icb, allerede var i gang. Disse filformater blev kodificeret, og et mindre bredt specifikt filformat TGA blev introduceret. TGA var en udvidelse til det, der allerede var i brug, og gav information såsom bredde, højde, pixeldybde, tilhørende farvekort og billedoprindelse.

TGA's 2.0 version, udgivet i 1989, inkorporerede flere forbedrede funktioner såsom:

 * Miniaturebilleder
 * Alfa kanal
 * Gamma værdi
 * Tekstmæssige metadata

De vigtigste bidragydere til TGA's 2.0-version inkluderer Truevisions Shawn Steiner, Kevin Fiedly og David Spoelstra.

## TGA TARGA filformatspecifikationer

En TGA-fil består af 2 hoveddele:

 * Header
 * Color Pixel-oplysninger

Alle værdierne i en TGA-fil er i little-endian i henhold til formatspecifikationerne.

### TGA-header

En TGA-filheader består af følgende 5 felter.

|Feltnr.|Længde |Feltnavn |Beskrivelse|
---|---|---|---|
|1| 1 byte |ID længde| Længde af billed-id-feltet (0-255)|
|2| 1 byte |Farvekorttype| Om et farvekort er inkluderet (0 - angiver, at ingen farvekortdata er inkluderet i dette billede. 1 - angiver, at et farvekort er inkluderet i dette billede.)|
|3| 1 byte |Billedtype| Kompression og farvetyper (0- Ingen billeddata inkluderet. 1- Ukomprimeret, Farvekortlagt billede, 2- Ukomprimeret, True Color Image, 9- Run-længdekodet, Farvekortlagt billede, 11- Run-Length-kodet, Sort-hvidt billede )|
|4| 5 bytes |Farvekortspecifikation| Beskriver farvekortet|
|5| 10 bytes |Billedspecifikation| Billedets dimensioner og format|

### Billed- og farvekortdata

|Feltnr. |Længde |Felt |Beskrivelse|
---|---|---|---|
|6 |Fra billed-ID-længdefelt| Billed-id| Valgfrit felt, der indeholder identificerende oplysninger|
|7 |Fra farvekortspecifikationsfelt| Farvekortdata| Opslagstabel indeholdende farvekortdata|
|8 |Fra billedspecifikationsfelt| Billeddata| Gemt i henhold til billedbeskrivelsen|

### Udviklerområde (valgfrit)

TGA Version 2.0 giver understøttelse af yderligere forbedringer/ekstraudstyr, som mange udviklere ønskede at gemme mere information. Informationen er valgfri, så hvis en TGA-dekoder ikke er i stand til at fortolke den, vil den blive ignoreret.

### Udvidelsesområde (valgfrit)

|Felt nr.| Længde| Felt |Beskrivelse|
---|---|---|---|
|10| 2 bytes |Udvidelsesstørrelse |Størrelse i bytes af udvidelsesområdet, altid 495|
|11| 41 bytes| Forfatternavn |Forfatterens navn. Hvis det ikke bruges, skal bytes sættes til NULL (\0) eller mellemrum|
|12| 324 bytes| Forfatterkommentar| En kommentar, organiseret som fire linjer, der hver består af 80 tegn plus en NULL|
|13| 12 bytes| Dato/tidsstempel |Dato og tidspunkt, hvor billedet blev oprettet|
|14| 41 bytes| Job ID||
|15| 6 bytes| Jobtid| Timer, minutter og sekunder brugt på at oprette filen (til fakturering osv.)|
|16| 41 bytes| Software ID |Det program, der oprettede filen.|
|17| 3 bytes| Softwareversion||
|18| 4 bytes| Nøglefarve||
|19| 4 bytes| Pixel billedformat||
|20| 4 bytes| Gammaværdi||
|21| 4 bytes| Farvekorrektionsforskydning |Antal bytes fra begyndelsen af filen til farvekorrektionstabellen, hvis den findes|
|22| 4 bytes| Frimærke | Antal bytes fra begyndelsen af filen til frimærkebilledet, hvis det findes|
|23| 4 bytes| Scan linje offset| Antal bytes fra begyndelsen af filen til scanningslinjetabellen, hvis den er til stede|
|24| 1 byte| Attributter type| Angiver alfakanalen|

### Filsidefod (valgfrit)

De sidste 26 bytes af filen repræsenterer sidefoden, hvilket betyder, at det sandsynligvis er en TGA version 2-fil.

|Felt nr.| Længde| Felt| Beskrivelse|
---|---|---|---|
|28| 4 bytes| Udvidelse offset| Offset i bytes fra begyndelsen af filen|
|29| 4 bytes| Udviklerområde offset| Offset i bytes fra begyndelsen af filen|
|30| 16 bytes| Signatur| Indeholder TRUEVISION-XFILE|
|31| 1 byte| | Indeholder .|
|32| 1 byte| | Indeholder NULL|


## Referencer

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA af Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

