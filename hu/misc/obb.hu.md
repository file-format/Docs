{
  "date" : "2022-02-16",
  "keywords" :[ "obb fájl", "obb fájlformátum", "mi az Obb fájl", "fájl", "obb példa", "obb fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB fájlformátum - Android átlátszatlan bináris blob fájl",
  "description":"További információ az OBB fájlformátumról és az API-król, amelyek OBB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Mi az OBB fájl?

Az OBB-fájl egy olyan bővítőfájl, amely az Android [APK](/hu/compression/apk/) fájlon kívül további adatokat is tartalmaz. A Google Play Áruház nem engedélyez 100 MB-nál nagyobb Android APK-fájlt. Egyes alkalmazások azonban nagy felbontású grafikákat, médiafájlokat vagy egyéb nagyméretű eszközöket igényelhetnek az APK-fájlok mellett. Itt jönnek be az OBB fájltípusok. A Google Play lehetővé teszi ezeknek a bővítőfájloknak az APK-fájl kiegészítéseként történő csatolását.

## OBB fájlformátum

Az OBB fájlok bináris fájlként kerülnek mentésre az APK fájlokkal együtt. Amikor egy APK kíséri az OBB fájlokat, a Google Play a bővítőfájlokat a szerverén tárolja, és a fejlesztőt nem terheli további költség. Ezeket a további fájlokat a rendszer az eszköz megosztott tárhelyén tárolja az SD-kártyán vagy az USB-re szerelhető partíción, amikor az alkalmazást letölti a telepítéshez.

Az OBB fájlok letöltése és telepítése a letöltéskor megtörténik. Bizonyos esetekben azonban ezek letöltésre kerülnek telepítésre az alkalmazás első futtatásakor.

### OBB maximális fájlméret

A Google Play Áruház lehetővé teszi akár 2 GB méretű OBB bővítőfájlok feltöltését. A nagy méretű fájlokat tömörített [ZIP](/hu/compression/zip/) fájlként javasoljuk feltölteni a hatékony internetes feltöltés érdekében.

Ezek a bővítőfájlok **fő** elsődleges bővítőfájlként tárolhatók az alkalmazás által igényelt további erőforrásokhoz, vagy opcionális javítási bővítőfájlként, amely a fő bővítőfájl kis frissítésére szolgál.

## Hivatkozások

* [Android fejlesztők – bővítőfájlok](https://developer.android.com/google/play/expansion-files)

