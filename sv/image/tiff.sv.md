{
  "date" : "2019-10-11",
  "keywords" :[ "tiff-fil", "tiff-filformat", "vad är en tiff-fil", "fil", "tiff-exempel", "tiff-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Bildfilformat",
  "description":"Läs mer om TIFF-filformat och API:er som kan skapa och öppna TIFF-filer.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en TIFF-fil?

TIFF eller TIF, Tagged Image File Format, representerar rasterbilder som är avsedda för användning på en mängd olika enheter som överensstämmer med denna filformatstandard. Den kan beskriva bilevel-, gråskala-, palett-färg- och fullfärgsbilddata i flera färgrymder. Den stöder såväl förlustfria som förlustfria komprimeringssystem för att välja mellan utrymme och tid för applikationer som använder formatet. Formatet är inte maskinberoende och är fritt från gränser som processor, operativsystem eller filsystem.

## Kort historik över TIFF-filformat

TIFF-filformatet skapades ursprungligen av Aldus Corporation hösten 1986, efter en serie möten med olika skannertillverkare och mjukvaruutvecklare. Det primära syftet med TIFF-filformatet var att tillhandahålla ett gemensamt skannat bildfilformat för alla leverantörer av skrivbordsskanner. Från och med stöd för endast binära bildformat, utvecklades formatet till stöd för gråskala och färgbilder med tidens gång. Den ursprungliga versionen av TIFF-filformatspecifikationerna kan märkas som Reivision 3.0 eftersom det fanns två tidigare utkast. En större version 5.0 publicerades 1988 som lade till stöd för palettfärgbilder och LZW-komprimering. Revision 6.0 av TIFF-filformat publicerades 1992 efter det. 1994 förvärvade Adobe Systems Aldus och specifikationerna är nu tillgängliga och underhålls av Adobe Systems.

## TIFF-filformatspecifikationer

TIFF-filformatet är utökningsbart och har genomgått flera revisioner som gör det möjligt att inkludera en obegränsad mängd privat eller specialinformation. En TIFF-fil börjar med en 8-byte header där byten är nummer från 0 till N. Den största möjliga TIFF-filen är 2**32 byte lång. Filen börjar med en 8-byte bildfilshuvud som pekar på en bildfil direkt (IFD). En IFD innehåller information om bilden samt pekare till den faktiska bilddatan.

### TIFF-filhuvud

8-byte TIFF-filhuvudet innehåller följande information:

**Byte 0-1:** Byteordningen som används i filen. Lagliga värden är: "II"(4949.H)"MM" (4D4D.H).

I formatet "II" är byteordningen alltid från den minst signifikanta byten till den mest signifikanta byten, för både 16-bitars och 32-bitars heltal. Detta kallas little-endian byteordning. I formatet "MM" är byteordningen alltid från mest signifikant till minst signifikant, för både 16-bitars och 32-bitars heltal. Detta kallas big-endian byte-ordning.

**Byte 2-3:** Ett godtyckligt men noggrant valt nummer (42) som ytterligare identifierar filen som en TIFF-fil. Byteordningen beror på värdet på Byte 0-1.

**Byte 4-7:** Offset (i byte) för den första IFD. Katalogen kan finnas var som helst i filen efter rubriken men måste börja på en ordgräns. I synnerhet kan en bildfilskatalog följa bilddata som den beskriver. Läsare måste följa pekarna vart de än leder. Termen byteoffset används alltid i detta dokument för att hänvisa till en plats i förhållande till början av TIFF-filen. Den första byten i filen har en offset på 0.

### Bildfilkatalog

En IFD innehåller information om bilden samt pekare till den faktiska bilddatan. Den består av en 2-byte räkning av antalet katalogposter (dvs antalet fält), följt av en sekvens av 12-byte fältposter , följt av en 4-byte offset av nästa IFD (eller 0 om ingen). Det måste finnas minst 1 IFD i en TIFF-fil och varje IFD måste ha minst en post.

#### IFD Entry

Varje 12-byte IFD-post har följande format.


|Byte|Beskrivning
---|---|
|0-1|Taggen som identifierar fältet
|2-3|Fälttypen
|4-7|Antal av den angivna typen
|8-11|Värdeförskjutningen, filförskjutningen (i byte) av värdet för fältet. Värdet förväntas börja på en ordgräns; motsvarande värdeförskjutning blir således ett jämnt tal. Denna filförskjutning kan peka var som helst i filen, även efter bilddata

Ett TIFF-fält är en logisk enhet som består av TIFF-taggen och dess värde. Detta logiska koncept implementeras som en IFD-post, plus det faktiska värdet om det inte passar in i värde/offset-delen, de sista 4 byten av IFD-posten. Termerna TIFF-fält och IFD-post är utbytbara i de flesta sammanhang.

### Baslinje TIFF ###

Baseline TIFF är kärnan i TIFF, det väsentliga som alla vanliga TIFF-utvecklare bör stödja i sina produkter. Överensstämmelse med TIFF-formatet är föremål för efterlevnad av Baseline TIFF-kraven. Dessa krav är väl dokumenterade i specifikationsdokumentet 6.0.

#### Flera bilder per fil ####

Det kan finnas mer än en IFD i en TIFF-fil. Varje IFD definierar en underfil. En potentiell användning av underfiler är att beskriva relaterade bilder, såsom sidorna i en faxöverföring. En Baseline TIFF-läsare krävs inte för att läsa några IFD:er utöver den första.

#### Bildtyper ####

Baseline TIFF Image har följande typer:

**Bilevel:** En bilevel-bild innehåller två färger – svart och vit. TIFF tillåter en applikation att skriva ut tvånivådata i antingen ett vitt-är-noll- eller svart-är-noll-format. Fältet som registrerar denna information kallas **Photometric Interpretation**.

* RGB fullfärg

Fotometrisk tolkningsinformation för Bilevel-bilder är följande:

Tag = 262 (106.H)
Typ = KORT
**Värden**

|Värde|Beskrivning|
---|---|
|0|För bilder med två nivåer och gråskala: 0 visas som vit. Det maximala värdet visas som svart. Detta är det normala värdet för Compression#2|
|1|BlackIsZero. För bilder med två nivåer och gråskala: 0 visas som svart. Det maximala värdet visas som vitt. Om detta värde anges för komprimering #2, bör bilden visas och skrivas ut omvänt.|

**Gråskala:** Gråskalabilder är en generalisering av tvånivåbilder. Bilevel-bilder kan endast lagra svartvita bilddata, men gråskalebilder kan också lagra gråtoner. För att beskriva sådana bilder måste du lägga till eller ändra följande fält. De andra obligatoriska fälten är desamma som de som krävs för tvånivåbilder. För gråskalebilder, komprimering # 1 eller 32773 (PackBits). I Baseline TIFF kan gråskalebilder antingen lagras som okomprimerad data eller komprimeras med PackBits-algoritmen.

**BitsPerSample** information för gråskalebilder är följande:

Tag = 258 (102.H)
Typ = KORT

Antalet bitar per komponent. Tillåtna värden för Baseline TIFF-gråskalebilder är 4 och 8, vilket tillåter antingen 16 eller 256 distinkta gråtoner.

**Palett-färg:** Palett-färgbilder liknar gråskalebilder. De har fortfarande en komponent per pixel, men komponentvärdet används som ett index i en fullständig RGB-uppslagstabell. För att beskriva sådana bilder måste du lägga till eller ändra följande fält. De andra obligatoriska fälten är desamma som för gråskalebilder.
Fotometrisk tolkningsinformation för Palett-Color-bild är som följer:

Fotometrisk tolkning = 3 (Palettfärg).
ColorMapTag = 320 (140.H)
Typ = KORT
N = 3 * (2 BitsPerSample)

Det här fältet definierar en röd-grön-blå färgkarta (ofta kallad en uppslagstabell) för palettfärgbilder. I en palett-färgbild används ett pixelvärde för att indexera till en RGB-uppslagstabell. Till exempel skulle en palettfärgpixel med värdet 0 visas enligt den 0:e röda, gröna, blå tripletten. I en TIFF ColorMap kommer alla röda värden först, följt av gröna värden och sedan blå värden. I ColorMap representeras svart av 0,0,0 och vitt representeras av 65535, 65535, 65535.

**RGB fullfärg:** I en RGB-bild består varje pixel av tre komponenter: röd, grön och blå. Det finns ingen ColorMap. För att beskriva en RGB-bild måste du lägga till eller ändra följande fält och värden. De andra obligatoriska fälten är desamma som de som krävs för palettfärgbilder.

BitsPerSample = 8,8,8. Varje komponent är 8 bitar djup i en Baseline TIFF RGB-bild.

Photometric Interpretation = 2 (RGB) och det finns ingen ColorMap.

Tag = 277 (115.H)
Typ = KORT
Antalet komponenter per pixel. Detta nummer är 3 för RGB-bilder, såvida inte extra prover finns.

## Referenser ##

* [TIFF-filformat - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

