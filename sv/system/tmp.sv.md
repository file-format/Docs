{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "tillägg", "fil", "format", "system", "TMP-fil", "TMP-dokument", "TMP-filer", "Tillfällig fil", "applikation", "program" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Tillfälligt filformat",
  "description":"Läs mer om TMP-filformat och API:er som kan skapa och öppna TMP-filer.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Vad är TMP fil? ##

En TMP-fil hänvisar till en tillfällig säkerhetskopiering, lagring eller annat filsystem som genereras av ett program. Den skapas ibland som en osynlig fil och förstörs ofta när programmet avslutas. TMP-filer kan också användas för att tillfälligt lagra information medan en ny fil konstrueras.

## TMP-filformat ##

En TMP-fil består vanligtvis av rådata som används som en fas i omvandlingsprocessen av material från en stil till en annan. Microsoft Word och Apple Safari är två appar som kan producera och använda TMP-filformat.

TMP-dokument som genereras bör i teorin tas bort automatiskt när programmet stängs eller maskinen stängs av. I praktiken är detta inte alltid fallet. Som ett resultat, när du navigerar genom ditt programs dokument, kan du stöta på övergående filer som inte aktivt används av systemet eller någon annan programvara.

### Extraminne ###

Virtuellt minne används i operativsystem, men program som använder stora mängder information kan behöva göra tillfälliga dokument.

### Kommunikation mellan processer ###

De flesta operativsystem tillhandahåller primitiver för att överföra data mellan program, såsom rör, sockets eller huvudminne, men den enklaste metoden är att överföra filer till en temporär fil och informera den mottagande ansökan om var den temporära filen var.


## Teknisk specifikation ##

Att erhålla distinkta temporära dokumentnamn tillhandahålls vanligtvis av operativsystem och program.
Tillfälliga filer kan skapas säkert på POSIX-system med hjälp av biblioteksfunktionerna mkstemp eller tmpfile. Vissa system inkluderar den tidigare POSIX (sedan borta) mktemp-applikationen. Dessa filer finns vanligtvis i den vanliga temporära katalogen på Unix-plattformar i /TMP, eller %TEMP% (det är specifikt för inloggning) på Windows-maskiner.

När programmet stoppas eller dokumentet stängs tas den transienta filen som genereras med tmp-filen automatiskt bort. GetTempFileName (Windows) eller tmpnam (POSIX) kan användas för att skapa ett temporärt filnamn som kommer att vara längre än programmet som skapade det.

## Referens ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
