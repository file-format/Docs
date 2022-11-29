{
  "date" : "2019-10-11",
  "keywords" :[ "tga fil", "tga filformat", "vad är en tga fil", "fil", "tga exempel", "tga filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA-filformat - En TARGA-grafisk bildfil",
  "description":"Läs mer om TGA-filformat och API:er som kan skapa och öppna TGA-filer.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en TGA fil?

En fil med filtillägget .tga är ett rastergrafikformat och skapades av Truevision Inc. Den designades för TARGA-korten (Truevision Advanced Raster Adapter) och gav stöd för Highcolor/truecolor-skärmar för IBM-kompatibla datorer. Den stöder 8, 16, 24 och 32 bitar per pixel och 8-bitars alfakanal. Den stöder också förlustfri RLE-komprimering som kan användas för att minska bildstorleken. Digitala foton och texturer använder TGA-bildformatet.

## Kortfattad bakgrund

Bildandet av TGA-filformat kom till 1984 av AT&T EPICenter (senare extraherad och bildad som en oberoende enhet känd som Truevision) som arbetade med marknadsföring av ny teknik utvecklad av AT&T för färgramsbuffertar. EPICenter arbetade redan på sina första två kort, VDA (Video Display Adapter) och ICB (bildfångstkort) för vilka arbete på två filtyper, .vda och .icb, redan var under bearbetning. Dessa filformat kodifierades och mindre brett specifika filformat TGA introducerades. TGA var en förlängning av det som redan användes och gav information som bredd, höjd, pixeldjup, tillhörande färgkarta och bildursprung.

TGA:s 2.0-version, publicerad 1989, innehöll flera förbättrade funktioner som:

* Miniatyrer
* Alfakanal
* Gammavärde
* Textuell metadata

De främsta bidragsgivarna till TGA:s 2.0-version inkluderar Truevisions Shawn Steiner, Kevin Fiedly och David Spoelstra.

## TGA TARGA filformatspecifikationer

En TGA-fil består av två huvuddelar:

* Header
* Information om färgpixlar

Alla värden i en TGA-fil är i little-endian enligt formatspecifikationerna.

### TGA-huvud

En TGA-filhuvud består av följande 5 fält.

|Fältnr|Längd |Fältnamn |Beskrivning|
---|---|---|---|
|1| 1 byte |ID-längd| Längd på bild-ID-fältet (0-255)|
|2| 1 byte |Färgkartatyp| Huruvida en färgkarta ingår (0 - anger att ingen färgkartasdata ingår i denna bild. 1 - anger att en färgkarta ingår i denna bild.)|
|3| 1 byte |Bildtyp| Kompressions- och färgtyper (0- Inga bilddata ingår. 1- Okomprimerad, färgmappad bild, 2- Okomprimerad, True Color Image, 9- Run-length-kodad, Färgmappad bild, 11- Run-Length-kodad, Svartvit bild )|
|4| 5 byte |Färgkartaspecifikation| Beskriver färgkartan|
|5| 10 bytes |Bildspecifikation| Bildmått och format|

### Bild- och färgkartadata

|Fält nr. |Längd |Fält |Beskrivning|
---|---|---|---|
|6 |Från bild-ID-längdfält| Bild ID| Valfritt fält som innehåller identifierande information|
|7 |Från färgkartaspecifikationsfält| Färgkartadata| Uppslagstabell som innehåller färgkartadata|
|8 |Från bildspecifikationsfält| Bilddata| Lagrat enligt bildbeskrivningen|

### Utvecklarområde (valfritt)

TGA Version 2.0 ger stöd för ytterligare förbättringar/tillägg som många utvecklare ville lagra mer information. Informationen är valfri så att om en TGA-avkodare inte kan tolka den kommer den att ignoreras.

### Förlängningsområde (valfritt)

|Fält nr.| Längd| Fält |Beskrivning|
---|---|---|---|
|10| 2 byte |Utökningsstorlek |Storlek i byte av tilläggsområdet, alltid 495|
|11| 41 byte| Författarens namn |Författarens namn. Om den inte används ska bytes sättas till NULL (\0) eller blanksteg|
|12| 324 byte| Författarkommentar| En kommentar, organiserad som fyra rader, var och en bestående av 80 tecken plus en NULL|
|13| 12 byte| Datum/tidsstämpel |Datum och tid då bilden skapades|
|14| 41 byte| Jobb-ID||
|15| 6 byte| Jobbtid| Timmar, minuter och sekunder spenderade på att skapa filen (för fakturering, etc.)|
|16| 41 byte| Programvaru-ID |Applikationen som skapade filen.|
|17| 3 byte| Programvaruversion||
|18| 4 byte| Nyckelfärg||
|19| 4 byte| Pixel bildförhållande||
|20| 4 byte| Gammavärde||
|21| 4 byte| Färgkorrigeringsoffset |Antal byte från början av filen till färgkorrigeringstabellen om sådan finns|
|22| 4 byte| Frimärke | Antal byte från början av filen till frimärksbilden om den finns|
|23| 4 byte| Scan line offset| Antal byte från början av filen till tabellen för skanningslinjer om den finns|
|24| 1 byte| Attributtyp| Anger alfakanalen|

### Filsidfot (valfritt)

De sista 26 byten av filen representerar sidfoten, vilket om det finns betyder att det troligen är en TGA version 2-fil.

|Fältnummer| Längd| Fält| Beskrivning|
---|---|---|---|
|28| 4 byte| Förlängningsförskjutning| Offset i byte från början av filen|
|29| 4 byte| Utvecklare område offset| Offset i byte från början av filen|
|30| 16 byte| Signatur| Innehåller "TRUEVISION-XFILE"|
|31| 1 byte| | Innehåller "."|
|32| 1 byte| | Innehåller NULL|


## Referenser

* [TGA 2.0 filformatspecifikationer](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA av Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

