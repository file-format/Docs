{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "bestand", "extensie", "format", "wat is een cue-bestand", "muziek", "cue-bestandsformaat", "specificatie cue-bestandsformaat", "cue-blad", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over CUE-bestandsindeling en API's die CUE-bestanden kunnen maken, converteren en openen.",
  "title" :"CUE - Cue Sheet-bestand",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Wat is een CUE-bestand?

Een bestand met de extensie .cue, ook wel cue sheet-bestand genoemd, is een metadatabestand dat informatie bevat over de lay-out van tracks op een cd of dvd. Deze worden ondersteund door mediaspelers en toepassingen voor het maken van optische schijven. De belangrijkste audiogegevens die op de cd zijn opgeslagen, worden verwezen door het cue-bestand, samen met de specificaties van tracklengtes, schijftitels en artiesten. Dus als een enkel audiobestand meerdere tracks bevat, kan het cue-bestand worden gebruikt om de audio in meerdere bestanden te verdelen of om naar verschillende tracks te verwijzen.

## CUE-bestandsindeling

CUE- of cue-sheetbestanden worden opgeslagen in platte tekst die voor mensen leesbaar is. Informatie in een cue-bestand zijn opdrachten met een of meer parameters. Deze commando's zijn van toepassing op het hele bestand of op een individuele track, afhankelijk van het specifieke commando en de context. De CDRWIN gebruikershandleiding beschrijft de specificaties voor de cue sheet syntax en semantiek.

## CUE-blad essentiële commando's

|Commando|Beschrijving|
---|---|
|BESTAND| Verwijst naar het bestand dat de gegevens bevat en het formaat ervan, zoals [MP3](/nl/audio/mp3/), [WAV](/nl/audio/wav/), of gewone binaire schijfafbeelding)|
|TRACK| Definieert de trackcontextinformatie zoals het nummer en type of modus.|
|INDEX| Vertegenwoordigt de positie als een index binnen het BESTAND. Het formaat is mm:ss:ff (minuut-seconde-frame).|
|PREGAP en POSTGAP|Dit geeft de pregap of post-gap van een track aan, die in geen enkel databestand is opgeslagen. De lengte wordt gespecificeerd in hetzelfde minuut-second-frame formaat als voor INDEX.|

### CUE-bladvoorbeeld

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
## Referenties

* [.cda-bestand - Door Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

