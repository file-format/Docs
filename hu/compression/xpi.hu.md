{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI – Cross-platform Installer Package File",
  "description":"További információ az XPI fájlformátumról és az API-król, amelyek XPI-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Mi az XPI fájl?

Az XPI-fájl egy telepítési archívum, amely tömörítve van a fájl méretének csökkentése érdekében. A Mozilla alkalmazások bővítmények és kiegészítő fájlok telepítésére használják. Tartalmaz egy telepítő szkriptet vagy egy jegyzéket a fájl gyökerében, valamint számos adatfájlt. Az XPI-fájlok tartalmazhatnak témákat, eszközkészletet vagy Firefox-bővítményeket, amelyeket a felhasználó telepíthet, hogy a Firefox böngésző, a Thunderbird vagy a SeaMonkey részévé váljon.

## XPI fájlformátum - További információ

Az XPI-fájlokat a rendszer [ZIP](/hu/compression/zip/) archívumként menti lemezre, amely több fájlt egyetlen tömörített fájlba egyesít. Az XPI-fájlban lévő fájlok tartalmazhatnak telepítő szkriptfájlt, például JS-t, és webfájlokat, például [CSS](/hu/web/css/), [HTML](/hu/web/html/) és [JSON](/hu/web/json/) ). Néha [PNG](/hu/image/png/) képfájlokat is tartalmazhat, amelyeket a kiegészítők ikonként használhatnak.

### Hogyan lehet megtekinteni az XPI fájl tartalmát?

Az XPI-fájl gyakorlatilag egy ZIP-archívum, amelynek tartalma a következő lépésekkel tekinthető meg.

* Módosítsa a fájl kiterjesztését XPI-ről ZIP-re
* Bontsa ki a fájl tartalmát bármely szabványos kicsomagoló segédprogrammal, például a WinZip (Windows, Mac), a 7-Zip (Windows) vagy az Apple Archive Utility (Mac) segítségével.

### Telepítse az XPI fájlt a Firefox Androidra

Leginkább az emberek kíváncsiak arra, hogy az XPI-fájlok telepíthetők-e a Firefoxban Android-eszközökön. Androidon XPI-fájlból telepíthet bővítményt úgy, hogy megkeresi a fájlt, és megnyitja a Firefox segítségével.

## Hivatkozások

* [XPInstall – Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Hogyan nyithatok meg XPI fájlkiterjesztést?](https://support.mozilla.org/en-US/questions/1009049)

