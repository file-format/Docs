{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ-filformat - Fritzing-delfil",
  "description":"Läs mer om vad en FZPZ-fil och API:er är som kan skapa och öppna FZPZ-filer.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Vad är en FZPZ fil?

En FZPZ-fil är en komponent/del som används i en elektronisk kretsdesign skapad med kretsprototyp- och designapplikationen **Fritzing**. Det är ett komprimerat arkiv som innehåller en [FZP](/sv/cad/fzp/) fil och fyra [SVG](/sv/page-description-language/svg/) bilder som beskriver den övergripande delen i Fritzing. Fördelen med att använda dessa filer är att användare kan dela sina FZPZ-filer med var och en ur återanvändbarhetssynpunkt. Att dela FZPZ-delar hjälper till att integrera kretsdelar för att skapa större PCB-designer på ett snabbt sätt.

## FZPZ-filformat - Mer information

FZPZ-filer sparas på skiva som komprimerade [ZIP](/sv/compression/zip/)-arkiv. Du kan byta namn på tillägget från .fzpz till .zip och använda vilket standardverktyg som helst för dekomprimering som WinZIP för att extrahera filerna från arkivet.

### FZPZ-filstrukturinformation

Som nämnts är en FZPZ-fil en arkivfil som innehåller flera filer för representation av en del som används i kretskort. FZPZ innehåller följande filer:

* "Fyra SVG-filer" - som representerar delens broadboard, schema, PCB och ikonbilder
* `FZP-fil` - En XML-fil som innehåller information om delens egenskaper, kopplingar och bussar

Filerna heter vanligtvis enligt följande.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Referenser ##

* [Nya delar med fzpz-tillägg](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

