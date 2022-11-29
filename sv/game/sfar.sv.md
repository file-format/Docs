{
  "date" : "2021-10-20",
  "keywords" :[ "sfar fil", "sfar filformat", "vad är en sfar fil", "fil", "sfar exempel", "Mass Effect 3 DLC filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om Mass Effect 3 SFAR-filformat och API:er som kan skapa och öppna SFAR-filer.",
  "title" :"SFAR - Mass Effect 3 DLC-fil",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Vad är SFAR fil?

En fil med tillägget .sfar är en speldatafil som används av Mass Effect 3 för att lagra dess DLC (nedladdningsbart innehåll) i ett komprimerat, proprietärt arkiv. Mass Effect 3 är ett spel skapat av Electronic Arts, ett ledande spelutvecklingsföretag. DLC-innehållet som lagras i en SFAR-fil används för att utöka spelet med ytterligare innehåll och funktioner.

## SFAR-filformat - Mer information

SFAR-filer lagras/sparas som komprimerade arkivfiler i binärt filformat. Dessa använder både LZX- och LZMA-komprimeringsalgoritmer för att komprimera innehållet. SFAR-filer kan öppnas med DLC Editor som levereras med ME3 Explorer. Förutom SFAR kan DLC Editor extrahera andra spelfiler som [PCC](/sv/game/pcc/).

## Specifikationer för SFAR-filformat

En SFAR-fil är uppdelad i följande fyra huvuddelar.

### SFAR Header

SFF Header innehåller information om de olika bitarna som utgör filen.

### SFAR-filtabell

SFAR-filtabellen innehåller en lista med filposter där varje post är 30 byte lång.

### Blockstorlekstabell

Block-Size innehåller flera poster, där varje post är 2 byes lång. Detta värde anger blockstorleken som motsvarar en post i filtabellen.

### Block

Blockbitar i en SFAR-fil innehåller data i SFAR-filen.

## Referenser

* [DLC SFAR File Format - Research](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

