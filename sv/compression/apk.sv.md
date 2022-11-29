{
  "date" : "2019-10-11",
  "keywords" :[ "apk-fil", "apk-filformat", "vad är en apk-fil", "fil", "apk-exempel", "apk-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Vad är en APK-fil?",
  "description":"Lär dig veta vad en APK-fil och API:er är som kan skapa och öppna APK-filer.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Vad är en APK-fil?

En fil med tillägget .apk är en Google Android-appfil som används för att installera appar (applikationer) på Android-enheterna. Den skapas som en körbar fil med den officiella IDE Google Android Studio, och laddas upp till Google Play Store för att laddas ner och installeras av slutanvändare. APK-filer kan genereras och göras tillgängliga för manuell installation innan de publiceras i Google Play Store. Detta hjälper till att testa funktionaliteten och beteendet hos den genererade APK-paketfilen. Därför måste man vara säker på att APK-filen kommer från en pålitlig källa och inte innehåller någon skadlig kod.

## APK-filformat

APK-filer är paketerade som komprimerade i [ZIP](/sv/compression/zip/) filformat som kan öppnas med valfri ZIP-filöppningsprogramvara. .apk-tillägget för en sådan fil kan döpas om till .zip och öppna filen i valfritt ZIP-program eller extrahera dess innehåll.

## APK-paketets innehåll

En enda APK-fil innehåller alla nödvändiga filer som krävs för installation och exekvering. En APK-fil, när den extraheras med ett ZIP-program, innehåller följande filer och mappar.

* `META-INF/`: Katalog som innehåller manifestfilen, signaturen och en lista över resurser i arkivet
* `lib/`: Katalog som innehåller kompilerad kod relaterad till specifika plattformar som armeabi-v7a, x86, arm64-v8a, etc.
* `res/`: Katalog som innehåller icke-kompilerade resurser såsom bilder
* `tillgångar/`: Katalog som innehåller programtillgångar, som kan hämtas av AssetManager.
* `androidManifest.xml`: Innehåller namn, versionsinformation och innehåll för APK-filen
* `classes.dex`: Dessa är kompilerade Java-klasser som kan köras på Dalvik virtuell maskin och av Android Runtime
* `resources.arsc`: Kompilerad resursfil såsom strängar

## Hur installerar jag APK-fil på Android-enhet?

För att installera en APK-fil på dina Android-enheter kan följande steg användas.

1. Ladda ner APK-filen med webbläsaren
2. Tryck på den – du bör då kunna se den laddas ner i den övre raden på din enhet
3. När den har laddats ner öppnar du Nedladdningar, trycker på APK-filen och trycker på Ja när du uppmanas.

Genom att följa dessa steg startar installationen av appen på din enhet.

## Referenser

* [APK-filformat](https://en.wikipedia.org/wiki/Android_application_package)

