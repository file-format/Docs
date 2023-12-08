{
"datum": "2023-05-16",
  "keywords": [
"samisk fil",
"vad är en samisk fil",
"exempel på samisk fil",
"fil",
"sami filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SAMI-filformat - Fil för undertexter och utbyte av metadata",
  "description":"Läs mer om SAMI-format och API:er som kan skapa och öppna SAMI-filer.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Vad är SAMI fil?

En fil med tillägget ".sami" hänvisar vanligtvis till en SAMI-fil (Subtitles And Metadata Interchange). SAMI är ett textningsformat som används för att visa undertexter i videor. Det utvecklades ursprungligen av Microsoft för deras Windows Media Player.

SAMI-filer innehåller tidsinformation och textinnehåll för undertexter, vilket gör att de kan synkroniseras med en videouppspelning. Formatet stöder grundläggande formateringsalternativ som typsnittsstil, färg och placering av undertexterna på skärmen.

SAMI-filer är vanligtvis vanliga textfiler och kan öppnas och redigeras med hjälp av en textredigerare. Innehållet i en SAMI-fil inkluderar vanligtvis en rubriksektion som ger information om filen, följt av individuella undertextposter med deras respektive timing och text.

Här är ett exempel på hur en SAMI-fil kan se ut:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI-filer används vanligtvis tillsammans med videospelare eller mediaspelare som stöder undertextvisning, som Windows Media Player eller VLC Media Player. Spelaren läser SAMI-filen och synkroniserar undertexterna med videoinnehållet, så att tittarna kan läsa undertexterna medan de tittar på videon.

## HTML-taggar som stöds

SAMI-filer (Subtitles And Metadata Interchange) stöder en begränsad uppsättning HTML-liknande taggar för formatering och styling av undertexterna. Här är några av de vanligaste taggar som stöds av SAMI:

- ``<SAMI> :`` Rotelementet som kapslar in hela SAMI-filen.
- ``<HEAD> :`` Innehåller rubrikinformation för SAMI-filen.
<html>- ``<TITLE> :`` Anger titeln på SAMI-filen. </html>
- ``<BODY> :`` Omsluter undertextposterna och deras tidsinformation.
- ``<SYNC> :`` Representerar en synkroniseringspunkt för en undertextpost. Den anger tidpunkten vid vilken undertexten ska visas.
- ``<P> :`` Omsluter det faktiska textinnehållet i en undertext. Det används vanligtvis inom en<SYNC> blockera.
<html>- `` <FONT>:`` Definierar teckensnittsegenskaper för den bifogade texten. Attribut som färg, ansikte, storlek och stil kan användas för att ändra teckensnittets utseende.</font>
- ``<BR> :`` Infogar en radbrytning i en undertext.
<html>- `` <B>:`` Gör den bifogade texten i fet stil.</b>
<html>- `` <I>:`` Återger den bifogade texten i kursiv stil.</i>
<html>- `` <U>:`` Gör den bifogade texten understruken.</u>
- ``<C> :`` Anger positionen eller justeringen av undertexten på skärmen. Den stöder attribut som Center, Middle, Left, Right, Top, Bottom och deras kombinationer.
- ``<LANG> :`` Anger språkkoden för undertexten. Det hjälper till att identifiera språket för undertexterna.

Det här är några av de grundläggande taggar som stöds av SAMI-filer. Det är viktigt att notera att SAMI inte stöder hela utbudet av HTML-taggar och attribut. De taggar som stöds är främst inriktade på att utforma och placera undertexterna snarare än att tillhandahålla omfattande dokumentstrukturering eller interaktivitet.

## Referenser
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

