{
  "date": "2021-08-11",
  "keywords": [
"vox",
"fil",
"udvidelse",
"format",
"lyd",
"ADPCM",
"Dialogisk ADPCM",
"Xentec VOX Studio",
"vox udvidelse",
"vox filer"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om VOX filformat og API'er, der kan oprette og åbne VOX filer.",
  "title": "VOX - lydfilformat",
  "linktitle": "VOX",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-vo-dax"
}
},
  "lastmod": "2021-08-11"
}

## Hvad er en VOX fil? ##

Ved en lav samplingshastighed er VOX-filerne specificeret til at gemme digitaliserede stemmedata. Disse er lydfiler, der almindeligvis bruges i de applikationer, der er specificeret til telefonisk kommunikation. Denne type filformat bruger en algoritme for tabskomprimering, som har en optimering til stemme.

Almindeligvis brugt i taleapplikationer indeholder VOX-filerne forudindspillede stemmemeddelelser. Denne type filformat konverteres også til andre mere populære formater. Disse kan bruges i Windows-operativsystemet og macOS.

Det bruges mest til stemmeoptagelser og komprimering. I dette format kan polyfoniske data ikke gemmes, da de kun understøtter homofobiske data.



## Kort historie ##

VOX-filerne er knyttet til Media Boards kaldet DMV og JCT of Dialogic. Disse tilhører VoxWare og meget anden software. Det plejede at blive betragtet som et forældet format.

Som et forældet format blev det ikke brugt derefter. I lighed med andre ADPCM-formater blev det komprimeret til 4 bit. Funktionerne i disse filer er tæt nok på [WAV](/audio/wav/) filspecifikationer.


## Formatspecifikationer ##

Denne type filformat er kompatibel med Windows OS-programmer såsom Xentec Vox Studio. Det har specifikke funktioner, der bruges til at stimulere menneskers tale. Arkadespil bruger for det meste dette format. VOX-filudvidelsen har en 32-byte header sammen med 10-byte indekser og rammer. De faktiske stemmedata gemmes i rammer i form af segmenter i en enkelt fil. Der er en forskellig form for flere bytes i hver frame baseret på typen af kodning.

Klargøringen af stemmen opretholdes ved en lav samplinghastighed, hvilket er sjældent i de fleste lydformater. Algoritmen, der blev brugt i disse, var matematisk.

Denne fil er kodet ved brug af ADPCM. Den kortslutter 16-bit lyddata og 4-bit komprimering. Så der er en fordel ved at gemme større lydinformation i en kompakt form ved hjælp af VOX-filer.


## Referencer ##

* [VOX - Af Wikipedia](https://en.wikipedia.org/wiki/Dialogic_ADPCM)


