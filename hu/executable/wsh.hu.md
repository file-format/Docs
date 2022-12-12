{
  "date" : "2021-08-27",
  "keywords" :[ "wsh fájl", "wsh fájl formátum", "mi az a wsh fájl", "fájl", "wsh példa", "wsh fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a WSH fájlformátumról és az API-król, amelyek WSH-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"WSH - Windows Script File",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Mi az a WSH fájl?
A .wsh kiterjesztésű fájl egy bizonyos programozási nyelvi szkript tulajdonságait és paramétereit tartalmazza, például VB vagy VBS stb. A WSH tényleges igénye, hogy ezeket bizonyos szkriptek végrehajtásának testreszabásához használja. A futtatáshoz WScript vagy CScript szükséges, és mindkettő benne van a Windows operációs rendszerben. A WSH-fájlok kezdetben a Windows 95 telepítőlemezein voltak a Vezérlőpulthoz opcionálisan konfigurálható és telepíthető elemként, majd a Windows 98 alapértelmezett összetevőjeként.

## WSH fájlformátum
A WSH (Windows Script Host) különféle célokra használható, beleértve az adminisztrációt, a bejelentkezési szkripteket és az általános automatizálást. A WSH környezetet hoz létre a szkriptek futtatásához. meghívja a megfelelő szkriptmotort, és lefoglal egy sor szolgáltatást és objektumot a szkript számára. Ezek a szkriptek GUI módban, COM objektumból vagy parancssori módban futtathatók, rugalmasságot biztosítva a felhasználónak az interaktív és nem interaktív parancsfájlokhoz egyaránt.

### Példák
Íme egy nagyon egyszerű példa, amely néhány VBScriptet mutat be, amely a "WScript" gyökér WSH COM objektumot használja az "OK" gombbal rendelkező üzenet megjelenítéséhez. Amikor ez a szkript elindul, a CScript vagy WScript motor meghívódik, és létrejön a futási környezet.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Hivatkozások

* [Windows Script Host – Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



