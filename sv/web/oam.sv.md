{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAM File - Adobe Edge Animate Widget File Format",
  "description" :"Läs mer om vad som är en OAM-fil och API:er som kan skapa och öppna OAM-fil.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Vad är en OAM fil?

En .oam-fil är en animerad widgetfil som exporteras från Adobe Edge Animate Widget. Animationer som exporteras som OAM-widgetfilformat kan infogas i andra Adobe-program som InDesign-dokument ([INDD-fil](/sv/page-description-language/indd/), Dreamweaver och Muse. OAM-filer är som distributionspaket som lätt kan användas infogas i andra Adobes projekt för att använda dem. OAM-filer innehåller information om animeringens tillgångar, beteenden och actionscript-kod. Du kan skapa en OAM-fil genom att publicera ett Adobe Animate-projekt [.AN-fil](/sv/web/an/) .
Användare kan skapa OAM-filer genom att publicera från ett Edge Animate-projekt (.AN-fil).

## OAM filformat

En OAM-fil sparas på skivan som komprimerat [ZIP](/sv/compression/zip/)-arkiv. Detta innebär att du kan byta namn på filtillägget till .zip och extrahera med valfritt komprimeringsverktyg som WinZIP eller WinRAR. Den minskade filstorleken gör det lättare att överföra och dela animationen med andra användare över internet.

### OAM-filstruktur

Den interna filstrukturen för en .oam-fil är proprietär och inte offentligt dokumenterad av Adobe. Det är dock känt att .oam-filer innehåller en samling filer och resurser (som grafik, ljud och ActionScript-kod) paketerade i en enda fil. Innehållet i en .oam-fil kan inkludera [XML](/sv/web/xml/)-filer, SWF-filer och andra resursfiler. Den exakta strukturen för .oam-filen beror på den specifika version av Adobe Animate som användes för att skapa den, såväl som typen av animering och tillgångar som ingår i filen.

En OAM-fil innehåller följande information.

`Tillgångar:` Information om grafik, ljud och videotillgångar som används i animeringen.

`Beteenden:` Beskrivningar av de åtgärder och interaktioner som sker i animeringen.

`ActionScript-kod:` Koden som används för att kontrollera animationens beteende och interaktivitet.

`Publiceringsinställningar:` Information om plattformen och formatet som animeringen kommer att publiceras i, som HTML5 eller AIR.

`Metadata:` Ytterligare information som animationens författare, datum för skapande och versionsnummer.

## Hur öppnar man filen OAM?

Du kan använda följande applikationer för att öppna OAM-filer.

* Adobe Edge Animate CC (upphört)
* Adobe Animate 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## Referenser

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)

