{
  "date": "2021-06-09",
  "keywords": [
"stikord",
"fil",
"udvidelse",
"format",
"hvad er en cue-fil",
"musik",
"cue filformat",
"cue-filformatspecifikation",
"cue sheet",
"CDRWIN"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CUE-filformat og API'er, der kan oprette, konvertere og åbne CUE-filer.",
  "title": "CUE - Cue Sheet File",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-dae"
}
},
  "lastmod": "2021-07-01"
}

## Hvad er en CUE fil?

En fil med filtypen .cue, også kendt som cue sheet-fil, er en metadatafil, der indeholder oplysninger om layoutet af spor på en cd eller dvd. Disse understøttes af medieafspillere og applikationer til oprettelse af optiske diske. De vigtigste lyddata, der er gemt på cd'en, refereres af cue-filen sammen med specifikationerne for sporlængder, disktitler og kunstnere. Så hvis en enkelt lydfil indeholder flere spor, kan cue-filen bruges til at opdele lyden i flere filer eller referere til forskellige spor.

## CUE filformat

CUE- eller cue sheet-filer gemmes i almindeligt tekstformat, der kan læses af mennesker. Information i en cue-fil er kommandoer med en eller flere parametre. Disse kommandoer gælder enten for hele filen eller til et individuelt spor, afhængigt af den bestemte kommando og konteksten. CDRWIN-brugervejledningen beskriver specifikationerne for cue-arkets syntaks og semantik.

## CUE Sheet Essential Commands

|Kommando|Beskrivelse|
---|---|
|FIL| Henviser til filen, der indeholder dataene og dets format, såsom [MP3](/audio/mp3/), [WAV](/audio/wav/) eller almindeligt binært diskbillede)|
|SPOR| Definerer sporkontekstinformationen, såsom nummer og type eller tilstand.|
|INDEKS| Repræsenterer positionen som et indeks i FILEN. Formatet er mm:ss:ff (minut-sekund-billede).|
|PREGAP og POSTGAP|Dette angiver pregap eller post-gap for et spor, som ikke er gemt i nogen datafil. Længden er angivet i samme minut-sekund-frame-format som for INDEX.|

### CUE Sheet Eksempel

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

## Andre CUE-filer

Her er andre filtyper, der bruger filtypen **.cue**.

**Disk og medier**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## Referencer

* [.cda-fil - af Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


