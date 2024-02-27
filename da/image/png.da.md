{
  "date": "2019-10-11",
  "keywords": [
"png fil",
"png filformat",
"hvad er en png-fil",
"fil",
"png eksempel",
"png filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PNG-filformat - rasterbilledfil",
  "description": "Lær om PNG-filformat og API'er, der kan oprette og åbne PNG-filer.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PNG fil?

En **PNG**-fil (Portable Network Graphics) er et rasterbilledfilformat, der bruger tabsfri komprimering. Dette filformat blev oprettet som en erstatning for Graphics Interchange Format ([GIF](/image/gif/)) og har ingen copyright-begrænsninger. PNG-filformatet understøtter dog ikke animationer. PNG-filformatet understøtter tabsfri billedkomprimering, hvilket gør det populært blandt sine brugere. Med tidens gang har PNG udviklet sig som et af de meget brugte billedfilformater.

## Kort historie om PNG-filformat

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Nøglehændelser med hensyn til PNG-filformater er angivet nedenfor:

* Oktober 1996: PNG-specifikationer version 1.0 blev frigivet og udkom senere som [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Det samme blev en W3C-anbefaling i oktober 1996.

* December 1998: Version 1.1, med nogle små ændringer og tilføjelse af tre nye bidder, blev frigivet.

* August 1999: Version 1.2, der tilføjede en ekstra del, blev frigivet.

* November 2003: PNG blev en international standard (ISO/IEC 15948:2003). Denne version af PNG adskiller sig kun lidt fra version 1.2 og tilføjer ingen nye bidder.

* Marts 2004: ISO/IEC 15948:2004


## Funktionel sammenligning af GIF og PNG

PNG-filformatet er designet til at være enkelt og bærbart, juridisk ubehæftet, udskifteligt, fleksibelt og robust. Følgende tabel viser de GIF-funktioner, der er nedarvet af PNG-filformat ud over nye funktioner.

|Funktion|GIF|PNG|
---|---|---|
|Indeksfarvebilleder med op til 256 farver|Ja|Ja|
|Support til streaming|Ja|Ja|
|Transparens|Ja|Ja|
|Supplerende oplysninger|Ja|Ja|
|Hardware og platformuafhængighed|Ja|Ja|
|Effektiv|Ja|Ja|
|Truecolor billeder på op til 48 bits pr. pixel|Nej|Ja|
|Gråtonebilleder på op til 16 bits pr. pixel|Nej|Ja|
|Fuld alfakanal (generelle gennemsigtighedsmasker)|Nej|Ja|
|Billed gamma information|Nej|Ja|
|Plidelighed|Nej|Ja|
|Hurtigere indledende præsentation|Nej|Ja|

## PNG-filstruktur

Næsten alle operativsystemer understøtter åbning af PNG-filer. For eksempel har Microsoft Windows viewer mulighed for at åbne PNG-filer, da operativsystemet som standard har den understøttelse, der er tilgængelig som en del af installationen. En PNG-fil består af en PNG-'signatur' efterfulgt af en række //chunks//.

### PNG-filoverskrift

De første otte bytes af en PNG-fil indeholder altid følgende (decimal) værdier:

{{{137 80 78 71 13 10 26 10 }}}

Denne signatur angiver, at resten af filen indeholder et enkelt PNG-billede, der består af en række bidder, der begynder med en IHDR-chunk og slutter med en IEND-chunk.

### Klumper ###

Hver del består af fire dele:

**Længde:** Et 4-byte heltal uden fortegn, der angiver antallet af bytes i chunkens datafelt. Længden tæller kun datafeltet, ikke sig selv, chunk type-koden eller CRC. Nul er en gyldig længde. Selvom indkodere og dekodere bør behandle længden som uden fortegn, må dens værdi ikke overstige 231 bytes.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Chunk Data:** Databytes, der passer til chunk-typen, hvis nogen. Dette felt kan være af nul længde.

**CRC:** En 4-byte CRC (Cyclic Redundancy Check) beregnet på de foregående bytes i chunken, inklusive chunktypekoden og chunkdatafelterne, men ikke inklusive længdefeltet. CRC er altid til stede, selv for bidder, der ikke indeholder data.

Klumpdatalængden kan være et hvilket som helst antal bytes op til maksimum; derfor kan implementere ikke antage, at chunks er justeret på nogen grænser, der er større end bytes.

Chunks kan vises i enhver rækkefølge, underlagt de begrænsninger, der er fastsat for hver chunk-type. (En bemærkelsesværdig begrænsning er, at IHDR skal vises først, og IEND skal vises sidst; IEND-klumpen fungerer således som en ende-på-fil-markør.) Flere bidder af samme type kan vises, men kun hvis det er specifikt tilladt for den type.

#### Klumptyper

Chunk-typerne er kategoriseret i **Kritiske** og **Ancillary**-bidder baseret på den 4-byte store og små ASCII-værdi, der er tildelt chunktypen. Alle implementeringer skal forstå og gengive standardkritiske bidder med succes. Et gyldigt PNG-billede skal indeholde en IHDR-chunk, en eller flere IDAT-chunks og en IEND-chunk.

### Kompression

PNG-komprimeringsmetode 0 (den eneste komprimeringsmetode, der i øjeblikket er defineret for PNG) specificerer deflater/pust komprimering med et glidende vindue på højst 32768 bytes. Deflate-komprimering er et LZ77-derivat, der bruges i zip, gzip, pkzip og relaterede programmer. Der er udført omfattende forskning, der understøtter dens patentfri status. De komprimerede data i zlib-datastrømmen lagres som en række blokke, som hver kan repræsentere rå (ukomprimerede) data, LZ77-komprimerede data kodet med faste Huffman-koder eller LZ77-komprimerede data kodet med brugerdefinerede Huffman-koder. En markørbit i den sidste blok identificerer den som den sidste blok, hvilket gør det muligt for dekoderen at genkende slutningen af den komprimerede datastrøm.

#### Forkomprimeringsfiltrering

Forkomprimeringsfiltre anvendes for at forberede billeddataene til optimal komprimering. PNG-filtermetoden definerer fem grundlæggende filtertyper som følger:

|Filtertype|Navn|Forventet værdi|
---|---|---|
|0|Ingen|Skanningslinjen sendes uændret|
|1|Sub|Transmitterer forskellen mellem hver byte og værdien af den tilsvarende byte for den foregående pixel.|
|2|Up|Up()-filteret er ligesom Sub()-filteret, bortset fra at pixlen umiddelbart over den aktuelle pixel, snarere end lige til venstre for den, bruges som forudsigelse.|
|3|Average|Average()-filteret bruger gennemsnittet af de to nabopixel (til venstre og over) til at forudsige værdien af en pixel.|
|4|Paeth|Paeth()-filteret beregner en simpel lineær funktion af de tre nabopixel (venstre, over, øverst til venstre), og vælger derefter som forudsigelse den nabopixel, der er tættest på den beregnede værdi.|

Filtreringsalgoritmer anvendes på bytes, ikke på pixels, uanset billedets bitdybde eller farvetype. Filtreringsalgoritmerne arbejder på bytesekvensen dannet af en scanline. Hvis billedet indeholder en alfakanal, filtreres alfadataene på samme måde som billeddataene.

Når billedet er interlaced, behandles hver passage af interlace-mønsteret som et uafhængigt billede til filtreringsformål. Filtrene arbejder på de bytesekvenser, der dannes af de pixels, der rent faktisk transmitteres under et gennemløb, og den forrige scanningslinje er den, der tidligere er transmitteret i samme gennemløb, ikke den, der støder op til det komplette billede. Bemærk, at underbilledet, der transmitteres i en gang, altid er rektangulært, men har mindre bredde og/eller højde end hele billedet. Filtrering anvendes ikke, når dette underbillede er tomt.

## Referencer ##

* [PNG - Hjemmeside](http://www.libpng.org/pub/png/)


