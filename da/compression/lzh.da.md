{
  "date": "2021-06-16",
  "keywords": [
"LZH",
"Komprimeret",
"Fil",
"Udvidelse",
"Filformat",
"Lempel-Ziv",
"Haruyasu",
"LHA"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZH filformat",
  "description": "Lær om LZH filformat og API'er, der kan oprette og åbne LZH filer.",
  "linktitle": "LZH",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-dah"
}
},
  "lastmod": "2021-06-16"
}

## Hvad er en LZH fil? ##

A file with .lzh and .lha extension usually relates to archive compression file format. This file format is the same as other file compression formats like [ZIP](/compression/zip/), [RAR](/compression/rar/), etc. The main purpose of these file formats is to reduce the size of the format for easily sending as well as to keep them together in compressed form. AS compare to other western companies LZH files are very popular in Japan and usually used for compressing video game data. The LZH add-on for Windows 7 is built into the Japanese version of Windows 7. Microsoft udgav først Microsoft Compressed (LZH) Folder Add-on til den japanske version af Windows XP. Dette filformat er implementeret med komprimeringsbestemmelser og funktioner, der bruges af Lempel-Ziv og Haruyasu algoritmen

## LZH-specifikation ##

Komprimeringsmetoden for et LZH-arkiv vises som en fem-byte tekststreng, såsom -lz1-. Disse er den tredje til syvende byte i den komprimerede fil.

|Specifikation|Beskrivelse|
---|---|
|Udvidelse | .lzh, .lha|
|Medietype| application/x-lzh-komprimeret|
|Skriv kode| LHA_ (LHA-MELLEMRUM)|
|UTI| public.archive.lha|
|Udviklet af| Haruyasu Yoshizaki (Yoshi)|
|Type| Kompression|
|Udvidet fra| LArc|

## Problemer med at åbne en LZH-fil ##

Følgende er de få problemer, der kan forårsage dårlig funktion af LZH-filformat:
  
* Filen kan være korrupt. For at løse dette problem skal du downloade filen igen eller bede afsenderen om at sende filen igen
* Den anden grund er inficeret fil i dette tilfælde scan filen korrekt
* Ukorrekte links til LZH-filen
  *	 Removal of the description of the LZH 
* Ikke nok hardwareressourcer
* Forældede drivere til udstyret

## Referencer ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
