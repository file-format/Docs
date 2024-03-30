{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT File Format - Quick Movie File",
  "keywords" :[ "QT", "QuickTime-video", "qt-format", "hur man spelar upp qt-filer", "Quick Movie File", "QTFF", "video", "Apple" ],
  "description":"Läs mer om QT-filformat och API:er som kan skapa och öppna QT-filer.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Vad är en QT fil?

En fil med filtillägget .qt är en multimediacontainerfil som används av QuickTime-ramverket för att lagra multimediafilinnehåll. QuickTime File Format (QTFF) har utvecklats av Apple Inc. och är en multimediacontainerfil som innehåller ljud, video eller text för uppspelning senare. Det är det valda formatet för utbyte av digitala medier mellan enheter, applikationer och operativsystem. QT-filer sparas också i formatet [MOV](/sv/video/mov/) som också utvecklades av Apple Inc. Några av applikationerna som kan öppna QT-filer inkluderar Apple QuickTime-spelare, VLC-mediaspelare och Media Player Classic med K- Lite Codec Pack.

## QT filformat

QTFF är objektorienterad som exponerar en flexibel samling objekt för enkel analys och expansion. Varje spår i en QT-fil innehåller en digitalt kodad mediaström eller en datareferens till mediaströmmen som finns i en annan fil. Den hierarkiska datastrukturen som består av objekt som kallas atomer fungerar som spårbehållare. Filformatspecifikationer för [QT-filformat](https://developer.apple.com/documentation/quicktime-file-format) är officiellt tillgängliga av Apple Inc för utvecklarens referens.

### Mediebeskrivning

Mediebeskrivningen för en QuickTime-fil lagras separat från mediadata. Information som antalet spår, videokomprimeringsformat och tidsinformation lagras i mediabeskrivningen (även känd som filmresurs, filmatom eller helt enkelt filmen). Mediedata refereras av ett index i denna mediestruktur. Mediadata är de faktiska exempeldata, som videoramar och ljudprover, som används i filmen.

### Atomer

Atom är den grundläggande enheten i QuickTime-filen. Det finns två huvudfält i vilken atom som helst före alla andra fält: Storleks- och Typfält. Storleksfältet visar storleken på atomen medan typfältet anger vilken typ av data som lagras i atomen. Av naturen är atomer hierarkiska vilket innebär att en atom kan innehålla andra atomer som fortfarande kan innehålla andra. Layouten för en provatom visas i följande bild.

Varje atom har två delar, rubrik och data. Rubriken innehåller storleks- och typfälten och datadelen innehåller den faktiska datan. Vidare förklaras varje fält nedan:

#### Atomstorlek

Atomens rubrik och innehåll indikeras av ett 32-bitars heltal känt som atomens storlek. Storleksfältet innehåller atomens storlek i byte, uttryckt i ett 32-bitars heltal utan tecken.

#### Atomtyp

Typen av atom visas också av ett 32-bitars heltal, som oftast behandlas som ett fyrteckenfält med knemoniskt värde, såsom 'moov' (0x6D6F6F76) för en filmatom, eller 'trak' (0x7472616B) för en spåratom. När atomtypen är känd tillåter den tolkning av dess data.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Filstruktur ##

QT/MOV-filer består av på varandra följande bitar. Varje chunk har en 8-byte-huvud: 4-byte chunk-storlek (big-endian, high-byte first) och 4-byte chunk-typ - en av fördefinierade signaturer: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "hoppa", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "klipp", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Första chunken är av typen "ftype" och har en undertyp vid offset 8. MOV definieras av undertyp som måste vara "qt". För att komponera MOV-filen behövs itererande bitar tills okänd typ upptäcks.

Här är ett exempel: När du inspekterar en exempel MOV-fils binära data är det uppenbart att den börjar med en signatur **ftyp** (hex: 66 74 79 70) vid offset 4, som definierar QuickTime Container File Type. Filens undertyp är **qt~_~_** (hex: 71 74 20 20) vilket pekar på MOV-filtypen. Det första blockstorleken är 32 (hex: 00 00 00 20, big-endian, hög byte först), storleken ligger vid offset 0. Vid offset 32 (hex: 20) finns den andra biten, som har en storlek på 8 och typ **mdat** (hex: 6D 64 61 74).

Nästa bit är placerad vid offset 32+8#40 (hex: 28) och har en storlek 3 263 028 (hex: 00 31 CA 34) och typ **mdat** (hex: 6D 64 61 74) vid offset 44 (hex 2C). Nästa bit är placerad vid offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) och har en storlek 21,189 (hex: 00 00 52 C5) och typ **moov** (hex: 6D 6F 6F 76) vid offset 1 836 019 574 (hex: 00 31 CA 60). Detta är den sista biten, så den totala filstorleken är 3,263,068+21,189#3,284,257 byte.

## Referenser ##

* [QT-filformat - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

