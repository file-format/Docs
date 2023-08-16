{
  "date" : "2020-08-20",
  "keywords" :[ "fnt-fil", "fnt-filformat", "vad är en fnt-fil", "fil", "fnt-exempel", "fnt-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows Font File",
  "description":"Läs mer om FNT-filformat och API:er som kan skapa och öppna FNT-filer.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Vad är FNT fil?

En fil med filtillägget .fnt är en teckensnittsfil som lagrar allmän teckensnittsinformation i Windows-operativsystem. FNT-filer har till största delen ersatts av filformaten TrueType (.TTF) och OpenType (.OTF), och är ett föråldrat typsnittsfilformat från och med nu. Dessa filer kan lagra en enstaka bedömare eller vektorteckensnitt. Alla enhetsdrivrutiner stöder Windows 2.x-teckensnitt. Men inte alla drivrutiner
stöder Windows 3.0-versionen.

## FNT filformat

FNT-filer kan lagra ett enda raster- eller vektorteckensnitt. Vektorformaten används oftare av GDI jämfört med rastret där varje charters glyph definieras med en liten bitmapp. Den uppenbara anledningen till att .fnt ersätts med .ttf och .otf är dess rasterformat.

### Font File Header
Början av både raster- och vektorteckensnittsfiler är vanlig, följt av olika information för varje filtyp. Teckensnittsfilens rubrik inkluderar för Windows 3.0 innehåller sex nya fält enligt följande som är nollställda för att säkerställa kompatibilitet med framtida versioner av Windows.

* dFlaggor
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

För detaljerad information om rubrikerna för Windows 3.0 och 2.0, besök [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Referenser
* [Teckensnittsfilformat](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Hur man installerar eller tar bort ett teckensnitt i Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

