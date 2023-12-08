{
"date": "2023-06-21",
  "keywords": [
"lrv-fil",
"vad är en lrv-fil",
"GoPro LRV-fil",
"THM File GoPro",
"hur man öppnar LRV-filer",
"fil",
"lrv filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LRV-filformat - Lågupplöst videofil av GoPro",
  "description":"Läs mer om LRV-format och API:er som kan skapa och öppna LRV-filer.",
  "linktitle": "LRV",
  "menu": {
    "docs": {
      "identifier": "video-lrv",
      "parent": "video"
}
},
"lastmod": "2023-06-21"
}

## Vad är en LRV fil?

En LRV-fil, även känd som lågupplöst videofil, är ett videofilformat som innehåller en version av video med lägre upplösning, som vanligtvis används i videoredigeringsarbetsflöden och videoproduktion för att skapa lågupplösta kopior av högupplösta videofiler. för att underlätta snabbare och smidigare redigeringsprocesser, särskilt när man arbetar med stora videofiler eller på system med begränsad processorkraft.

LRV-filer genereras vanligtvis av kamerasystem, såsom GoPro-kameror, som skapar en version med lägre upplösning av originalvideo under inspelningsprocessen, vilket gör det möjligt för användare att snabbt granska bilder, utföra grundläggande redigeringsuppgifter och göra val utan att behöva hantera större, höga -upplösningsfiler.

LRV-filformatet använder ofta H.264- eller H.265-videokomprimeringskodekar för att minska filstorleken med bibehållen rimlig kvalitetsnivå, men de kan fortfarande ge en anständig förhandsvisning av innehållet. Oavsett kamerans inställningar spelas LRV-video genomgående in med en upplösning på 240p med en bildhastighet på 29,97 bilder per sekund.

## GoPro LRV-fil

GoPro-kameror genererar LRV-filer (Low-Resolution Video) som en del av inspelningsprocessen. LRV-filer skapas tillsammans med högupplösta videofiler (vanligtvis i MP4-format) och fungerar som proxyservrar av lägre kvalitet för enklare och snabbare redigering.

Syftet med LRV-filer i GoPro-kameror är att tillhandahålla en lätt version av den inspelade filmen som enkelt kan hanteras genom att redigera programvara och system med begränsad processorkraft. Dessa filer tillåter användare att förhandsgranska och redigera sina videor utan att behöva arbeta direkt med de större högupplösta filerna, vilket kan vara resurskrävande.

GoPro LRV-filer har vanligtvis lägre upplösningar, reducerade bithastigheter och komprimerade codecs jämfört med de ursprungliga högupplösta filerna. De fungerar som visuella referenser under redigeringsprocessen och möjliggör mjukare uppspelning och skrubbning i redigeringsprogram.

När du redigerar med GoPro-material känner de flesta videoredigeringsprogram automatiskt igen LRV-filerna som är associerade med högupplösta videor. Denna sömlösa integration tillåter användare att redigera med proxyfilerna och sedan länka om det slutliga projektet till högupplösta filer för rendering och export.

## THM-fil GoPro

THM-filer är små miniatyrfiler som genereras av GoPro-kameror. Dessa filer skapas tillsammans med motsvarande videofiler och fungerar som visuella förhandsvisningar eller miniatyrer för enklare identifiering och organisering av det inspelade materialet.

När du spelar in en video med en GoPro-kamera genererar den en THM-fil med samma basnamn som videofilen men med filtillägget .THM. Om du till exempel har en video med namnet "example.MP4", skulle motsvarande miniatyrbildsfil vara "example.THM".

THM-filer är vanligtvis små i storlek och innehåller en lågupplöst bild som representerar en bildruta från motsvarande video. De kan visas med vilken bildvisare eller mediaspelare som helst som stöder JPEG-bildformatet.

Huvudsyftet med THM-filer är att ge en snabb visuell referens för att identifiera innehållet i de associerade videofilerna utan att behöva spela eller öppna dem. De används ofta för att bläddra och organisera bilder på GoPro-kameror eller när du överför filer till en dator.

## Hur öppnar man LRV-filer?

För att öppna och visa LRV-filer (Low-Resolution Video) kan du följa dessa steg:

- **Byt namn till MP4:** För att öppna och spela en LRV-fil kan du enkelt göra det genom att byta namn på filtillägget till [.MP4](/sv/video/mp4/) och använda valfritt program som kan spela upp .MPEG4-videofiler .

- **Videoredigeringsprogram:** Det vanligaste sättet att öppna och arbeta med LRV-filer är att använda videoredigeringsprogram. De flesta professionella videoredigeringsprogram, som _Adobe Premiere Pro_, _Final Cut Pro_ eller _Davinci Resolve_, kan känna igen och importera LRV-filer. Importera helt enkelt LRV-filerna till ditt projekt så kommer du att kunna förhandsgranska och redigera materialet.

- **GoPro-programvara:** GoPro tillhandahåller sin egen mjukvara som heter _GoPro Quik_, som är utformad speciellt för att arbeta med GoPro-material. Du kan ladda ner och installera GoPro Quik från den officiella GoPro-webbplatsen. När du har installerat den öppnar du programvaran, importerar dina LRV-filer och du kommer att kunna visa och redigera dem i programmet.

- **Mediaspelare:** Även om LRV-filer vanligtvis inte är avsedda för direkt uppspelning, kan du använda vissa mediaspelare som kan spela dessa filer. _VLC_ mediaspelare är ett populärt val som stöder olika videoformat och codecs. Du kan ladda ner och installera VLC och sedan öppna LRV-filen direkt via mediaspelaren.

- **Filkonvertering:** Om du föredrar att konvertera LRV-filer till ett videoformat som stöds mer, kan du använda programvara för videokonvertering. Verktyg som _Handbrake_ eller _Freemake Video Converter_ låter dig konvertera LRV-filer till format som [MP4](/sv/video/mp4/), som kan öppnas av ett brett utbud av mediaspelare eller videoredigeringsprogram.

## Referenser
* [GoPro LRV- och THM-filer](https://shotkit.com/lrv-thm-file/)

