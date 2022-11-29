{
  "date" : "2019-10-11",
  "keywords" :[ "mov-fil", "mov-filformat", "vad är en mov-fil", "fil", "mov-exempel", "mov-filtillägg", "tillägg", "format", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV-fil - Apple QuickTime Movie File Format",
  "description":"Läs mer om MOV-filformat och API:er som kan skapa och öppna MOV-filer.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Vad är en MOV-fil?

En MOV-fil är en videofiltyp, utvecklad av Apple Inc., som innehåller ett eller flera spår. Varje spår lagrar en film, ljud, filmklipp och undertexter. Det är en multimediabehållare som kan lagra olika typer av mediaelement. MOV-videoformatet är kompatibelt med både Windows- och Macintosh-system. Den använder MPEG-4 kodad för komprimering och spår upprätthålls i objekt som kallas atomer som placeras i en hierarkisk datastruktur.

## Kort historia av MOV-filformat

MPEG-4-filformatet har utvecklats från specifikationen QuickTime File Format (**QTFF**) 2001. International Organization of Standardization godkände formatet och MPEG-4 Part 1-systemspecifikationerna publicerades 1999. 2001, en revisionsfil format [MP4](/sv/video/mp4/) publicerades.

MP4:s första version reviderades 2003 som MPEG-4 Part 14 (ISO/IEC 14496-14:2003). 2004 generaliserades MP4 för att definiera en allmän struktur för alla tidsbaserade mediefiler. Därför används den nu som grund för olika andra multimediafilformat.

## QuickTime File Format (QTFF) - Mer information

För att kunna arbeta med digital multimedia kan QTFF hålla många typer av data. Det är ett idéformat för utbyte av digitala medier eftersom formatet definierar standarderna för att beskriva alla typer av mediestrukturer. Filformatet består av en flexibel samling objektorienterade objekt. För lagring av filmer på diskar använder QuickTime två strukturer, dvs "atomer" och "QT-atomer".

### Atomer

Atom är den grundläggande enheten i QuickTime-filen. Det finns två huvudfält i vilken atom som helst före alla andra fält: Storleks- och Typfält. Storleksfältet visar storleken på atomen medan typfältet anger vilken typ av data som lagras i atomen. Av naturen är atomer hierarkiska vilket innebär att en atom kan innehålla andra atomer som fortfarande kan innehålla andra. Layouten för en provatom visas i följande bild.

Varje atom har två delar, "header" och "data". Rubriken innehåller storleks- och typfälten och datadelen innehåller den faktiska datan. Vidare förklaras varje fält nedan:

### Atomstorlek

Atomens rubrik och innehåll indikeras av ett 32-bitars heltal känt som atomens storlek. Storleksfältet innehåller atomens storlek i byte, uttryckt i ett 32-bitars heltal utan tecken.

### Atomtyp

Typen av atom visas också av ett 32-bitars heltal, som oftast behandlas som ett fyrteckenfält med knemoniskt värde, som "moov" (0x6D6F6F76) för en filmatom, eller "trak" (0x7472616B) för en spåratom. När atomtypen är känd tillåter den tolkning av dess data.

### QT-atomer och atombehållare

QT-atomer tillhandahåller ett allmänt lagringsformat och har en utökad rubrik som består av fälten Storlek, Typ, Atom-ID och Antal barnatomer. QT-atomer är inslagna i en atombehållare, en unik datastruktur som har en rubrik med ett låsantal. Det finns en rotatom i varje atombehållare som är QT-atomen. Layouten för QT-atomen visas i figuren nedan.

QT atom container header har följande data:

Reserverat: Ett 10-byte-element med värdet 0.

Låsantal: 16-bitars heltal med värdet 0.

QT-atomhuvuden har följande data:

**Storlek -** QT-atomhuvud och innehåll indikeras i byte med ett 32-bitars heltal. I fallet med en lövatom innehåller detta fält storleken på en enda atom.

**Typ -** Typ av atom indikeras med ett 32-bitars heltal. Om det är rotatomen sätts värdet till "sean".

**Atom-ID -** Det är ett 32-bitars heltal som visar atom-ID och måste vara unikt för alla syskon. Rotatom alltid värdet på atom ID som 1.

**Reserverad -** Ett 16-bitars heltal som måste sättas till 0.

**Antal barn -** Ett 16-bitars heltal som anger antalet underordnade atomer i en atom.

**Reserverad -** Ett 32-bitars heltal som måste sättas till 0.

## Filstruktur för MOV-filer

MOV-filer består av på varandra följande bitar. Varje chunk har en 8-byte-huvud: 4-byte chunk-storlek (big-endian, high-byte first) och 4-byte chunk-typ - en av fördefinierade signaturer: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "hoppa", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "klipp", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Första chunken är av typen "ftype" och har en undertyp vid offset 8. MOV definieras av undertyp som måste vara "qt". För att komponera MOV-filen behövs itererande bitar tills okänd typ upptäcks.

Här är ett `exempelexempel`: När man inspekterar en exempel MOV-fils binära data är det uppenbart att den börjar med en signatur **ftyp** (hex: 66 74 79 70) vid offset 4, som definierar QuickTime Container File Type. Filens undertyp är **qt~_~_** (hex: 71 74 20 20) vilket pekar på MOV-filtypen. Det första blockstorleken är 32 (hex: 00 00 00 20, big-endian, hög byte först), storleken ligger vid offset 0. Vid offset 32 (hex: 20) finns den andra biten, som har en storlek på 8 och typ **mdat** (hex: 6D 64 61 74).

Nästa bit är placerad vid offset 32+8#40 (hex: 28) och har en storlek 3 263 028 (hex: 00 31 CA 34) och typ **mdat** (hex: 6D 64 61 74) vid offset 44 (hex : 2C). Nästa bit är placerad vid offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) och har en storlek 21,189 (hex: 00 00 52 C5) och typ **moov** (hex: 6D 6F 6F 76) vid offset 1 836 019 574 (hex: 00 31 CA 60). Detta är den sista biten, så den totala filstorleken är 3,263,068+21,189#3,284,257 byte.

## Hur konverterar man MOV-fil?

Det finns gott om mediaspelare och videoredigerare för programvara för att konvertera MOV-filer till andra populära videofilformat. Några av de mediaspelare som kan konvertera MOV-filer till andra format inkluderar:

* VideoLAN VLC mediaspelare
* Eltima Elmedia Player

Flera mediaspelare och videoredigerare, inklusive VideoLAN VLC mediaspelare och Eltima Elmedia Player, kan konvertera MOV-filer till andra format. Dessa program kan konvertera MOV-filer till följande videoformat.

* MPEG-4 Video - [MP4](/sv/video/mp4/)
* WebM Video - [WEBM](/sv/video/webm/)
* Videotransportström - [TS](/sv/video/ts/)
* Avancerat systemformat - [ASF](/sv/video/ts/)
* Ogg Vorbis Audio - [OGG](/sv/audio/ogg/)
* MP3-ljud - [MP3](/sv/audio/mp3/)
* Gratis förlustfri ljudkodek - [FLAC](/sv/audio/flac/)
* WAVE Audio - [WAV](/sv/audio/wav/)

## Open Source API för MOV-filer

* [React Native API för att konvertera MOV till MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API för att reparera MOV-filer](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API för att konvertera MOV till GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referenser

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

