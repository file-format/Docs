{
  "date" : "2019-10-11",
  "keywords" :[ "png-fil", "png-filformat", "vad är en png-fil", "fil", "png-exempel", "png-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG-filformat - rasterbildsfil",
  "description":"Läs mer om PNG-filformat och API:er som kan skapa och öppna PNG-filer.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PNG-fil?

En **PNG**-fil (Portable Network Graphics) är ett rasterbildsfilformat som använder förlustfri komprimering. Det här filformatet skapades som en ersättning för Graphics Interchange Format ([GIF](/sv/image/gif/)) och har inga upphovsrättsliga begränsningar. PNG-filformat stöder dock inte animationer. PNG-filformatet stöder förlustfri bildkomprimering vilket gör det populärt bland sina användare. Med tidens gång har PNG utvecklats som ett av de mycket använda bildfilformaten.

## Kort historik över PNG-filformat

Det främsta skälet bakom skapandet av PNG-filformatet var den patenterade komprimeringsalgoritmen, Lempel-Ziv-Welch, som används i GIF-filformatet. Detta tillsammans med andra GIF-begränsningar skapade ett behov av att ersätta [**GIF**](/sv/image/gif/) filformat. Det första förslaget och namnet för PNG-filformat kom i januari 1995. Viktiga händelser med avseende på PNG-filformat listas nedan:

* Oktober 1996: PNG-specifikationer version 1.0 släpptes och dök senare upp som [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Detsamma blev en W3C-rekommendation i oktober 1996.
* December 1998: Version 1.1, med några små ändringar och tillägg av tre nya bitar, släpptes.
* Augusti 1999: Version 1.2, med en extra bit, släpptes.
* November 2003: PNG blev en internationell standard (ISO/IEC 15948:2003). Denna version av PNG skiljer sig endast något från version 1.2 och lägger till inga nya bitar.
* Mars 2004: ISO/IEC 15948:2004

## Funktionell jämförelse av GIF och PNG

PNG-filformatet har utformats för att vara enkelt och portabelt, juridiskt obehindrat, utbytbart, flexibelt och robust. Följande tabell listar de GIF-funktioner som ärvs av PNG-filformat förutom nya funktioner.

|Funktion|GIF|PNG|
---|---|---|
|Indexfärgbilder med upp till 256 färger|Ja|Ja|
|Stöd för streaming|Ja|Ja|
|Transparens|Ja|Ja|
|Tilläggsinformation|Ja|Ja|
|Hårdvara och plattformsoberoende|Ja|Ja|
|Effektiv|Ja|Ja|
|Truecolor-bilder på upp till 48 bitar per pixel|Nej|Ja|
|Gråskalebilder på upp till 16 bitar per pixel|Nej|Ja|
|Fullständig alfakanal (allmänna transparensmasker)|Nej|Ja|
|Bildgammainformation|Nej|Ja|
|Tillförlitlighet|Nej|Ja|
|Snabbare initial presentation|Nej|Ja|

## PNG-filstruktur

Nästan alla operativsystem har stöd för att öppna PNG-filer. Till exempel har Microsoft Windows Viewer förmågan att öppna PNG-filer eftersom operativsystemet som standard har stödet tillgängligt som en del av installationen. En PNG-fil består av en PNG-`signatur` följt av en serie //chunks//.

### PNG-filhuvud

De första åtta byten i en PNG-fil innehåller alltid följande (decimala) värden:

{{{137 80 78 71 13 10 26 10 }}}

Denna signatur indikerar att resten av filen innehåller en enda PNG-bild, bestående av en serie bitar som börjar med en IHDR-bit och slutar med en IEND-bit.

### bitar ###

Varje bit består av fyra delar:

**Längd:** Ett 4-byte osignerat heltal som anger antalet byte i bitens datafält. Längden räknar endast datafältet, inte sig själv, koden för bittyp eller CRC. Noll är en giltig längd. Även om kodare och avkodare bör behandla längden som osignerad, får dess värde inte överstiga 231 byte.

**Chunk Type:** En 4-byte chunk typ kod. För att underlätta beskrivning och granskning av PNG-filer är typkoder begränsade till att bestå av stora och små ASCII-bokstäver (AZ och az, eller 65-90 och 97-122 decimaler). Kodare och avkodare måste dock behandla koderna som fasta binära värden, inte teckensträngar. Till exempel skulle det inte vara korrekt att representera typkoden IDAT med EBCDIC-motsvarigheterna till dessa bokstäver. Ytterligare namnkonventioner för chunktyper diskuteras i nästa avsnitt.

**Chunk Data:** Databyten som är lämpliga för chunktypen, om någon. Detta fält kan ha noll längd.

**CRC:** En 4-byte CRC (Cyclic Redundancy Check) beräknad på föregående byte i chunken, inklusive chunktypkoden och chunkdatafälten, men inte inklusive längdfältet. CRC är alltid närvarande, även för bitar som inte innehåller några data.

Databitens längd kan vara valfritt antal byte upp till det maximala; Därför kan implementörer inte anta att bitar är justerade på några gränser som är större än byte.

Bitar kan visas i valfri ordning, med förbehåll för de begränsningar som gäller för varje bittyp. (En anmärkningsvärd begränsning är att IHDR måste visas först och IEND måste visas sist, sålunda fungerar IEND-biten som en markör för slutet av filen.) Flera bitar av samma typ kan visas, men bara om det är specifikt tillåtet för den typen.

#### Bittyper

Chunktyperna kategoriseras i **Kritiska** och **Ancillary**-bitar baserat på det 4-byte skiftlägeskänsliga ASCII-värdet som tilldelats Chunk Type. Alla implementeringar måste förstå och framgångsrikt återge standardkritiska bitar. En giltig PNG-bild måste innehålla en IHDR-bit, en eller flera IDAT-bitar och en IEND-bit.

### Kompression

PNG-komprimeringsmetod 0 (den enda komprimeringsmetoden som för närvarande definieras för PNG) specificerar tömnings-/uppblåsningskompression med ett glidande fönster på högst 32768 byte. Deflate compression är en LZ77-derivata som används i zip, gzip, pkzip och relaterade program. Omfattande forskning har gjorts för att stödja dess patentfria status. Den komprimerade datan inom zlib-dataströmmen lagras som en serie block, som vart och ett kan representera rådata (okomprimerad), LZ77-komprimerad data kodad med fasta Huffman-koder eller LZ77-komprimerad data kodad med anpassade Huffman-koder. En markörbit i det sista blocket identifierar det som det sista blocket, vilket tillåter avkodaren att känna igen slutet av den komprimerade dataströmmen.

#### Förkomprimeringsfiltrering

Förkomprimeringsfilter används för att förbereda bilddata för optimal komprimering. PNG-filtermetoden definierar fem grundläggande filtertyper enligt följande:

|Filtertyp|Namn|Förutsagt värde|
---|---|---|
|0|Ingen|Skanningslinjen sänds oförändrad|
|1|Sub|Sänder skillnaden mellan varje byte och värdet på motsvarande byte för föregående pixel.|
|2|Up|Up()-filtret är precis som Sub()-filtret förutom att pixeln omedelbart ovanför den aktuella pixeln, snarare än bara till vänster om den, används som prediktor.|
|3|Average|Average()-filtret använder genomsnittet av de två angränsande pixlarna (vänster och ovanför) för att förutsäga värdet på en pixel.|
|4|Paeth|Paeth()-filtret beräknar en enkel linjär funktion av de tre angränsande pixlarna (vänster, ovan, övre vänstra), och väljer sedan som prediktor den angränsande pixel som ligger närmast det beräknade värdet.|

Filtreringsalgoritmer tillämpas på "bytes", inte på pixlar, oavsett bitdjup eller färgtyp på bilden. Filtreringsalgoritmerna arbetar på bytesekvensen som bildas av en skanningslinje. Om bilden innehåller en alfakanal filtreras alfadata på samma sätt som bilddata.

När bilden är sammanflätad behandlas varje pass av sammanflätningsmönstret som en oberoende bild för filtreringsändamål. Filtren arbetar på de bytesekvenser som bildas av de pixlar som faktiskt sänds under ett pass, och den "föregående skanningslinjen" är den som tidigare sänts i samma pass, inte den som ligger intill i hela bilden. Observera att underbilden som sänds i ett pass alltid är rektangulär, men har mindre bredd och/eller höjd än hela bilden. Filtrering tillämpas inte när denna underbild är tom.

## Referenser ##

* [PNG - Hemsida](http://www.libpng.org/pub/png/)

