{
  "date" : "2019-10-11",
  "keywords" :[ "b6z fil", "b6z filformat", "vad är en b6z fil", "fil", "b6z exempel", "b6z filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP arkivfilformat",
  "description":"Läs mer om B6Z-filformat och API:er som kan skapa och öppna B6Z-filer.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Vad är en B6Z fil?

En fil med filtillägget .b6z är en komprimerad arkivfil skapad macOS-programvara [B6Zip](http://b6zip.com) som används för att komprimera och dekomprimera filer. Det är ett relativt nytt arkivformat som tillåter högre komprimeringsgrad. B6Z har öppen arkitektur och stöder filstorlekar upp till 900000 PB. Den stöder datakomprimering, felåterställning och filspännande. Verktygsprogrammet B6Zip är tillgängligt gratis på MacOS för att öppna olika typer av komprimerade filer inklusive B6Z.

## B6Z filformat

B6Z-filformatet är baserat på öppen arkitektur och ger solid komprimering med AES-256 krypteringsalgoritm. Den använder LZMA2 som standardkomprimeringsmetod, men stöder även andra komprimeringsmetoder enligt följande.

|Metod|Beskrivning|
---|---|
|LZMA |Optimerad version av LZ77-algoritmen|
|LZMA2| Förbättrad version av LZMA|
|Tömma luft| Vanlig LZ77-algoritm|
|BZip2| Standard BWT-algoritm|
|PPMD| Dmitry Shkarins PPMdH|

Verktyget B6Zip stöder alla dessa komprimeringsstandarder och är mycket optimerat vilket resulterar i hög hastighet. Den stöder arbete med filformaten [ZIP](/sv/compression/zip/), [TAR](/sv/compression/tar/) och [RAR](/sv/compression/rar/). B6Z-filer har MIME-typ application/x-b6z-komprimerade.

## Referenser

* [B6Zip](http://b6zip.com)

