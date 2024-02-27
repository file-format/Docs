{
  "date": "2021-07-15",
  "keywords": [
"LNK",
"udvidelse",
"fil",
"format",
"system",
"LNK fil",
"link",
"LNK filer",
"LNK dokumenter",
"Ansøgning",
"programmer"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LNK - Link filformat",
  "description": "Lær om LNK filformat og API'er, der kan oprette og åbne LNK filer.",
  "linktitle": "LNK",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ln-dak"
}
},
  "lastmod": "2021-07-15"
}

## Hvad er LNK fil? ##

En LNK-fil, analogt med en identitet på Mac-systemet, er et Windows-alternativ eller link, der fungerer som en forbindelse til en original billeddokumentmappe eller -program. Den indeholder genvejsdestinationens type, position og filnavn samt programmet, der åbner måldokumentet og en ekstra genvejstast.

I Windows skal du rette en fil, mappe eller eksekverbart program og vælge Opret genvej. Placeringen af filformatet og mappen Begyndelse er to grundlæggende funktioner i LNK-filer. Filformatet for LNK-filer er maskeret, og en buet pil indikerer, at de er genveje.

## LNK filformat ##

LNK-filformater har normalt det samme ikon som deres destinationsfiler, men med tilføjelsen af en lille krøllet pil for at vise, at filen peger på en anden placering. Når genvejen dobbeltklikkes, opfører den sig, som om brugeren havde dobbeltklikket på den aktuelle fil.

LNK-filer, der indeholder programgenveje, kan have egenskaber, der påvirker, hvordan programmet kører. For at ændre attributterne skal du højreklikke på genvejsfilen og vælge **Egenskaber** og derefter ændre feltet Mål.

I stedet for at være filtypenavne er LNK-filer Windows Stifinder-udvidelser. Som en terminaludvidelse kan .lnk-dokumenter kun bruges i Windows Stifinder til at erstatte en fil, og de har andre formål i Windows Stifinder udover at tjene som en genvej til et lokalt dokument. Disse filer starter også med bogstavet L.

Mens genveje linker til bestemte filer og mapper, når de oprettes, kan de blive ubrugelige, hvis målet ændres til en anden placering. Explorer vil begynde at reparere en genvejsmappe, der peger på et dødt mål, når den åbnes.


## Teknisk specifikation ##

Kun når mappevisningsindstillingen Skjul udvidelser for genkendte filtyper ikke er markeret, viser Windows ikke .lnk-dokumentudvidelsen for dokumentgenveje. Selvom det ikke tilrådes, kan du aktivere filtypenavnet til at blive vist ved at fjerne egenskaben NeverShowExt fra HKEY_CLASSES_ROOT\lnk-filen i Windows registreringsdatabasen.

For at gøre det skal du tage disse trin:

* Åbn Registration Editor ved at indtaste Regedit i proceslinjens søgefelt og vælge programmet
* I applikationen skal du navigere til Computer\HKEY HKEY_CLASSES_ROOT\lnkfilplaceringen
* Lav en sikkerhedskopi af elementet ved at højreklikke på det og vælge Eksporter
* Vælg og slet NeverShowExt attributten
* Windows skal genstartes


## Reference ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
