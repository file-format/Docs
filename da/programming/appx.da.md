{
  "date": "2021-04-22",
  "keywords": [
"appx fil",
"udvidelse",
"format",
"hvordan man åbner appx fil",
"appx filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPX - Hvad er en APPX fil?",
  "description": "Lær om APPX-filformat og API'er, der kan oprette og åbne APPX-filer.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-dax"
}
},
  "lastmod": "2021-12-16"
}

## Hvad er en APPX fil?

En APPX-fil er et distribuerbart pakkefilformat, der bruges til distribution og installation af et program. Det blev introduceret med Windows 8 for at blive udgivet på Microsoft Windows Store. Den indeholder alle de filer, der kræves for at installere et Windows-program. Disse omfatter metadata, filer og legitimationsoplysninger. Et mere moderne pakkefilformat er MSIX, der i øjeblikket er mere almindeligt brugt sammenlignet med APPX.

## APPX-filformat - flere oplysninger

APPX-filer gemmes som komprimerede filer i filformatet [ZIP](/compression/zip/). Dette gør hele pakken som en arkivfil med reduceret filstørrelse, der er let at uploade til Microsoft Store.

## Hvordan får man vist filer i en APPX-fil?

For at se indholdet eller filerne i en APPX-fil, skal følgende trin følges.

 1. Da APPX-filer gemmes som komprimerede ZIP-filer, skal du omdøbe filen til filtypenavnet .zip
 1. Brug et hvilket som helst dekomprimeringsværktøj såsom 7-Zip, WinZip eller WinRAR til at udpakke filerne i APPX-filen

## Hvordan opretter man en APPX-fil?

Der er to metoder, der kan bruges til at oprette APPX-filer.

 1. Brug af MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) bruges til at oprette både apppakker (.msix eller .appx) og apppakkepakkefiler .msixbundle eller .appxbundle). Derudover kan den udtrække filer fra en app-pakke. MakeApp.exe er tilgængelig med Windows 10 SDK og kan bruges fra kommandoprompt.
 1. Brug af Microsoft Visual Studio - Udviklere [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview), der normalt bruger Microsoft Visual Studio. Når applikationsudviklingen er færdig, og appen er klar til at blive publiceret, kan APPX-pakkefilen oprettes ved at udgive den fra Visual Studio.

## Referencer

 * [Opret en MSIX-pakke eller pakke med MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Opret APPX-filer ved hjælp af Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

