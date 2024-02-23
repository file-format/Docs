{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om OSZ-filformat och API:er som kan skapa och öppna OSZ-filer.",
  "title" : "OSZ-fil - osu! Beatmap filformat",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz-sv",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är en OSZ fil?

En OSZ-fil är ett komprimerat filformat som används av rytmspelet osu! för att lagra beatmap-data. Beatmaps är i huvudsak nivåer för spelet, och de innehåller information som låten, taktimingen och placeringen av träffade objekt på spelskärmen. OSZ-filer möjliggör enkel distribution av beatmaps och laddas vanligtvis ner från internet och importeras till spelet. OSU! har även filformatet [OSR](/game/osr/) som är en omspelningsfil och kan spelas upp av spelarna.

**MIME-typ av OSR-filformat:** x-osu-replay

## OSZ filformat

De interna filformatsdetaljerna för OSZ-filtyper är inte tillgängliga offentligt. Den innehåller [ZIP](/compression/zip/)-komprimerad data som har information för att spela musik, visa grafik och visa spelare om händelserna när de måste interagera med spelet.

## Hur skapar jag OSZ-fil?

OSU! har detaljerade instruktioner för [creating OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files)- och OSK-filer. Följande steg kan användas för att skapa en OSZ-fil med OSU!.

1. Öppna en beatmap via editorn.
1. Från toppmenyn väljer du Arkiv > Exportera paket....
1. .osz-arkivet kommer att placeras i mappen Exports inuti osu! mapp.

## Referenser

* [OSU! Rhythm Game](https://osu.ppy.sh/home)


