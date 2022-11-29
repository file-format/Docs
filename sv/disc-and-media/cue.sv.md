{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "fil", "tillägg", "format", "vad är en cue-fil", "musik", "cue-filformat", "cue-filformatspecifikation", "cue sheet", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om CUE-filformat och API:er som kan skapa, konvertera och öppna CUE-filer.",
  "title" :"CUE - Cue Sheet File",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Vad är en CUE fil?

En fil med tillägget .cue, även känd som cue sheet-fil, är en metadatafil som innehåller information om layouten för spår på en CD eller DVD. Dessa stöds av mediaspelare och applikationer för att skapa optiska skivor. Huvudljuddata som lagras på CD:n refereras av cue-filen, tillsammans med specifikationerna för spårlängder, skivtitlar och artister. Om en enda ljudfil innehåller flera spår, kan cue-filen användas för att dela upp ljudet i flera filer eller referera till olika spår.

## CUE-filformat

CUE- eller cue sheet-filer lagras i vanligt textformat som är läsbart för människor. Information i en cue-fil är kommandon med en eller flera parametrar. Dessa kommandon gäller antingen för hela filen eller för ett enskilt spår, beroende på det specifika kommandot och sammanhanget. CDRWIN-användarhandboken beskriver specifikationerna för cue sheet-syntax och semantik.

## CUE Sheet Essential Commands

|Kommando|Beskrivning|
---|---|
|FIL| Avser filen som innehåller data och dess format såsom [MP3](/sv/audio/mp3/), [WAV](/sv/audio/wav/), eller vanlig binär skivbild)|
|SPÅR| Definierar spårkontextinformationen såsom dess nummer och typ eller läge.|
|INDEX| Representerar positionen som ett index i FILEN. Formatet är mm:ss:ff (minut-sekund-bildruta).|
|PREGAP och POSTGAP|Detta indikerar pregap eller post-gap för ett spår, som inte lagras i någon datafil. Längden anges i samma minut-sekund-bildrutaformat som för INDEX.|

### Exempel på CUE-ark

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referenser

* [.cda-fil - av Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

