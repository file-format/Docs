{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Vad är en APPX-fil?",
  "description":"Läs mer om APPX-filformat och API:er som kan skapa och öppna APPX-filer.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Vad är en APPX fil?

En APPX-fil är ett distribuerbart paketfilformat som används för distribution och installation av en applikation. Den introducerades med Windows 8 för att publiceras på Microsoft Windows Store. Den innehåller alla filer som krävs för att installera ett Windows-program. Dessa inkluderar metadata, filer och autentiseringsuppgifter. Ett mer modernt paketeringsfilformat är MSIX som för närvarande är vanligare jämfört med APPX.

## APPX-filformat - Mer information

APPX-filer sparas som komprimerade filer i filformatet [ZIP](/sv/compression/zip/). Detta gör hela paketet som en arkivfil med reducerad filstorlek som är lätt att ladda upp till Microsoft Store.

## Hur visar man filer i en APPX-fil?

För att se innehållet eller filerna i en APPX-fil bör följande steg följas.

1. Eftersom APPX-filer lagras som komprimerade ZIP-filer, byt namn på filen till filtillägget .zip
1. Använd valfritt dekomprimeringsverktyg som 7-Zip, WinZip eller WinRAR för att extrahera filerna i APPX-filen

## Hur skapar man en APPX-fil?

Det finns två metoder som kan användas för att skapa APPX-filer.

1. Använda MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) används för att skapa både apppaket (.msix eller .appx) och apppaketpaketfiler .msixbundle eller .appxbundle). Dessutom kan den extrahera filer från ett apppaket. MakeApp.exe är tillgängligt med Windows 10 SDK och kan användas från kommandotolken.
1. Använda Microsoft Visual Studio – Utvecklare [skapar vanligtvis APPX-filer](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) med Microsoft Visual Studio. När applikationsutvecklingen är klar och appen är redo att publiceras, kan APPX-paketfilen skapas genom att publicera den från Visual Studio.

## Referenser

* [Skapa ett MSIX-paket eller -paket med MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Skapa APPX-filer med Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

