{
  "date" : "2019-10-11",
  "keywords" :[ "apk fájl", "apk fájlformátum", "mi az apk fájl", "fájl", "apk példa", "apk fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Mi az APK-fájl?",
  "description":"Tanulja meg, hogy mi az APK-fájl és az API-k, amelyek APK-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Mi az APK fájl?

Az .apk kiterjesztésű fájl egy Google Android-alkalmazásfájl, amelyet alkalmazások (alkalmazások) Android-eszközökre történő telepítésére használnak. Futtatható fájlként jön létre a hivatalos IDE Google Android Studio segítségével, és feltöltődik a Google Play Áruházba, hogy a végfelhasználók letölthessék és telepítsék. Az APK-fájlok generálhatók és elérhetővé tehetők manuális telepítéshez, valamint a Google Play Áruházban való közzététel előtt. Ez segít a generált APK-csomagfájl működésének és viselkedésének tesztelésében. Ezért meg kell bizonyosodni arról, hogy az APK fájl megbízható forrásból származik, és nem tartalmaz rosszindulatú programokat.

## APK fájl formátum

Az APK-fájlok tömörített formában vannak csomagolva [ZIP](/hu/compression/zip/) fájlformátumban, amely bármely ZIP-fájlnyitó szoftverrel megnyitható. Az ilyen fájlok .apk kiterjesztése átnevezhető .zip-re, és megnyithatja a fájlt bármely ZIP-alkalmazásban, vagy kibonthatja a tartalmát.

## Az APK csomag tartalma

Egyetlen APK fájl tartalmazza az összes szükséges fájlt, amely szükséges a telepítéshez és végrehajtáshoz. Az APK-fájl ZIP-alkalmazással kicsomagolva a következő fájlokat és mappákat tartalmazza.

* `META-INF/`: a jegyzékfájlt, az aláírást és az archívumban lévő erőforrások listáját tartalmazó könyvtár
* `lib/`: Adott platformokhoz kapcsolódó lefordított kódot tartalmazó könyvtár, például armeabi-v7a, x86, arm64-v8a stb.
* `res/`: Nem lefordított erőforrásokat, például képeket tartalmazó könyvtár
* `assets/`: Alkalmazási eszközöket tartalmazó könyvtár, amelyet az AssetManager lekérhet.
* `androidManifest.xml`: Az APK-fájl nevét, verziószámítási információit és tartalmát tartalmazza
* `classes.dex`: Ezek olyan lefordított Java osztályok, amelyek futtathatók Dalvik virtuális gépen és az Android Runtime segítségével
* `resources.arsc`: Lefordított erőforrásfájl, például karakterláncok

## Hogyan telepíthetek APK fájlt Android-eszközre?

Az APK-fájl Android-eszközeire való telepítéséhez a következő lépéseket használhatja.

1. Töltse le az APK-t webböngészővel
2. Koppintson rá – ekkor látnia kell a letöltést a készülék felső sávjában
3. A letöltés után nyissa meg a Letöltések elemet, érintse meg az APK-fájlt, majd érintse meg az Igen gombot, amikor a rendszer kéri.

Az alábbi lépések végrehajtásával megkezdődik az alkalmazás telepítése az eszközön.

## Hivatkozások

* [APK fájlformátum](https://en.wikipedia.org/wiki/Android_application_package)

