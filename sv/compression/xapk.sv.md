{
  "date" : "2021-04-11",
  "keywords" :[ "xapk-fil", "xapk-filformat", "vad är en xapk-fil", "fil", "xapk-exempel", "xapk-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - Meta Package File Format",
  "description":"Läs mer om XAPK-filformat och API:er som kan skapa och öppna XAPK-filer.",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## Vad är en XAPK fil?

En fil med tillägget .xapk är en komprimerad paketfil som används för att installera Android-appar på mobila enheter. Det är ett containerfilformat som innehåller APK och ytterligare tillhörande filer som krävs för installationen. Den andra associerade filen är en OBB-fil som lagrar ytterligare filer som grafik, mediefiler och appdata som krävs för att hålla applikationen igång. XAPK-filer stöds inte av Google Play och används endast för distribution på tredje parts webbplatser för nedladdning av Android-appar. Dessa kan installeras på en Android-enhet med XAPK Installer.

## XAPK-filformat

XAPK-filer komprimeras med standardfilformatet [ZIP](/sv/compression/zip/). Dessa kan extraheras med hjälp av ett standardprogram för komprimering/dekomprimering som WinZIP. När XAPK-filen har extraherats till skivan, innehåller den följande filer i mappen.

* APK - Standardinstallationsfil för installation av applikationen på Android-enheter
* OBB - Ytterligare fil som innehåller relevanta resursfiler

## Referenser

* [Android-paketfil](https://en.wikipedia.org/wiki/Android_application_package)

