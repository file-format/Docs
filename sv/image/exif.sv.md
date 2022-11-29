{
  "date" : "2019-10-11",
  "keywords" :[ "exif-fil", "exif-filformat", "vad är en exif-fil", "fil", "exif-exempel", "exif-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Läs mer om EXIF-filformat och API:er som kan skapa och öppna EXIF-filer.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en EXIF fil?
EXIF står för "Exchangeable Image File Format", definitionen som först gavs av [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) 1985. Standarden hanteras av Japan Electronics och Information Technology Industries Association (JEITA) från och med idag. EXIF är en standard för specifikationer för bild- och ljudformat som främst används av digitalkameror och skannrar.

EXIF-standarden inkluderar taggning och metadatainformation med bildfilen. Metadata kan innehålla information som kameramodell, slutartid, datum och tid, bländare, tillverkare, exponeringstid, X-upplösning, Y-upplösning etc. Normalt döljs EXIF-data som standard. För att se EXIF-data måste man välja vyegenskaper i bildvisningsapplikationen. Exif-metadata kan också innehålla miniatyrer tillsammans med tekniska och primära bilddata i en enda bildfil.

## Historik och versioner ##

* I oktober 1995 etablerade JEIDA version 1. I denna version definierade JEIDA strukturen, som består av bilddataformat och attributinformation, och grundläggande taggar.
* Nov 1997, version 1.1 introducerades med de flesta taggar från version 1 men lade även till bestämmelser för valfri attributinformation och formatoperation.
* Juni 1998, version 2 med sRGB-färgrymd, komprimerade miniatyrer och ljudfiler.
* December 1998, version 2.1 med förbättrad lagring och attributinformation.
* Februari 2002, version 2.2, förbättrad version 2.1 med tillägg av utskriftsefterbehandling.
* September 2003, version 2.21 med valfri färgrymd känd som adobe RGB.

## EXIF-filformat

EXIF använder följande filformat med tillägg av specifik metadata.

1. [JPEG](/sv/image/jpeg/) - diskret cosinustransform (DCT) för komprimerade bildfiler.
1. [TIFF](/sv/image/tiff/) Rev. 6.0 (RGB eller YCbCr) för okomprimerade bildfiler.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) för ljudfiler (linjär [PCM](https:/ /en.wikipedia.org/wiki/Pulse-code_modulation) eller ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM för okomprimerad ljuddata, och [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) för komprimerad ljuddata).

### Markör som används av EXIF ###

Markören 0xFFE0~~0xFFEF är "Application Marker", som används av användarapplikationen. Till exempel använder äldre digi-kameror JFIF (JPEG File Interchange Format) för att lagra bilder. JFIF använder APP0 (0xFFE0) Marker för att infoga digi cam-konfigurationsdata och miniatyrbild. Vidare använder EXIF också en Application Marker för att infoga data, men EXIF använder APP1 (0xFFE1) Marker för att undvika en konflikt med JFIF-formatet. Alla EXIF-filformat startar från detta format.


|SOI-markör|APP1-markör|APP1-data|Övriga markörer
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Den startar från SOI (0xFFD8) Marker, så det är en JPEG-fil. Sedan följer APP1 Marker direkt. All data från EXIF lagras i detta APP1-dataområde. Delen av "SSSS" på den övre tabellen betyder storleken på APP1-dataområdet (EXIF-dataområdet). Observera att storleken "SSSS" inkluderar storleken på själva deskriptorn. Efter "SSSS" startar APP1-data. Den första delen är en speciell data för identifiering om EXIF eller inte, ASCII-tecken "EXIF" och 2 byte av 0x00 används. Efter APP1-markörområdet följer de andra JPEG-markörerna.

### Exif-datastruktur ###

En grov struktur för EXIF-data (APP1) visas enligt nedan. Som diskuterats ovan börjar EXIF-data från ASCII-tecknet "EXIF" och 2 byte på 0x00, sedan följer EXIF-data. EXIF använder TIFF-format för att lagra data.


|FFE1|APP1 Markör
---|---|
|SSSS|APP1 Data|APP1 Datastorlek
|45786966 0000|Exif Header
|49492A00 08000000|TIFF-huvud
|XXXX. . . .|IFD0 (huvudbild)|Katalog
|LLLLLLLL|Länk till IFD1
|XXXX. . . .|Dataområde för IFD0
|XXXX. . . .|Exif SubIFD|Katalog
|00000000|Länkens slut
|XXXX. . . .|Dataområde för Exif SubIFD
|XXXX. . . .|IFD1(miniatyrbild)|Katalog
|00000000|Länkens slut
|XXXX. . . .|Dataområde för IFD1
|FFD8XXXX. . . XXXXFFD9|Miniatyrbild

#### TIFF Header ####

8-byte [TIFF](/sv/image/tiff/) filhuvudet innehåller följande information:

`Byte 0-1:` Byteordningen som används i filen. Lagliga värden är: "II"(4949.H)"MM" (4D4D.H).

I formatet "II" är byteordningen alltid från den minst signifikanta byten till den mest signifikanta byten, för både 16-bitars och 32-bitars heltal. Detta kallas little-endian byteordning. I formatet "MM" är byteordningen alltid från mest signifikant till minst signifikant, för både 16-bitars och 32-bitars heltal. Detta kallas big-endian byte-ordning.

`Bytes 2-3:` Ett godtyckligt men noggrant utvalt nummer (42) som ytterligare identifierar filen som en TIFF-fil. Byteordningen beror på värdet på Byte 0-1.

`Byte 4-7:` Offset (i byte) för den första IFD. Katalogen kan finnas var som helst i filen efter rubriken men måste börja på en ordgräns. I synnerhet kan en bildfilskatalog följa bilddata som den beskriver. Läsare måste följa pekarna vart de än leder. Termen byteoffset används alltid i detta dokument för att referera till en plats i förhållande till början av TIFF-filen. Den första byten i filen har en offset på 0.

#### Bildfilkatalog ####

En IFD innehåller information om bilden såväl som pekare till de faktiska bilddata. Den består av en 2-byte räkning av antalet katalogposter (dvs antalet fält), följt av en sekvens av 12-byte fältposter , följt av en 4-byte offset av nästa IFD (eller 0 om ingen). Det måste finnas minst 1 IFD i en TIFF-fil och varje IFD måste ha minst en post.

##### IFD-post #####

Varje 12-byte IFD-post har följande format.


|Byte|Beskrivning
---|---|
|0-1|Taggen som identifierar fältet
|2-3|Fälttypen
|4-7|Antal av den angivna typen
|8-11|Värdeförskjutningen, filförskjutningen (i byte) av värdet för fältet. Värdet förväntas börja på en ordgräns; motsvarande värdeförskjutning blir således ett jämnt tal. Denna filoffset kan peka var som helst i filen, även efter bilddata

Ett TIFF-fält är en logisk enhet som består av TIFF-taggen och dess värde. Detta logiska koncept implementeras som en IFD-post, plus det faktiska värdet om det inte passar in i värde/offset-delen, de sista 4 byten av IFD-posten. Termerna TIFF-fält och IFD-post är utbytbara i de flesta sammanhang.

#### Tumnagel bild ####

Exif-formatet innehåller miniatyrer av bilden (förutom Ricoh RDC-300Z). Vanligtvis ligger den bredvid IFD1. Det finns 3 format för miniatyrer; JPEG-format (JPEG använder YCbCr), RGB TIFF-format, YCbCr TIFF-format.

##### JPEG-format miniatyrbild #####

Om värdet för Compression(0x0103) Tag i IFD1 är '6', är miniatyrbildsformatet JPEG. De flesta Exif-bilder använder JPEG-format för miniatyrbilder. I så fall kan du få förskjutning av miniatyrbilden med JpegIFOffset(0x0201) Tag i IFD1, storleken på miniatyren av JpegIFByteCount(0x0202) Tag. Dataformatet är vanligt JPEG-format, börjar från 0xFFD8 och slutar med 0xFFD9. Det verkar som att JPEG-format och storleken 160x120 pixlar rekommenderas miniatyrformat för Exif2.1 eller senare.

##### TIFF-format miniatyrbild #####

Om värdet för Compression(0x0103) Tag i IFD1 är '1', är miniatyrbildsformatet ingen komprimering (kallas TIFF-bild). Startpunkten för miniatyrbildsdata är StripOffset(0x0111) Tag, storleken på miniatyrbilden är summan av StripByteCounts(0x0117) Tag.

## Referenser ##

* [EXIF - av Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [EXIF-filformat](https://www.media.mit.edu/pia/Research/deepview/exif.html)

