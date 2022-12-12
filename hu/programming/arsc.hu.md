{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "mi az arsc fájl", "arsc fájl megnyitása", "kiterjesztés", "fájl", "arsc fájl", "arsc fájlformátum", "arsc fájl kiterjesztése", "arsc fájl példa"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android Package Resource Table File",
  "description":"További információ az ARSC fájlformátumról és az API-król, amelyek létrehozhatnak és megnyithatnak ARSC fájlt.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Mi az ARSC fájl?

Az ARSC-fájl egy Android-erőforrás-táblafájl, amely táblázatos formátumban tartalmazza az alkalmazás erőforráslistáját. Ez olyan információkat tartalmaz, mint az erőforrások nevei, tulajdonságai és azonosítói. Az ARSC-fájlok az ezen Android-alkalmazások telepítéséhez használt APK-csomagok részét képezik. Az Android-alkalmazásokban található összes erőforrás, például képek, elrendezések, stílusok és karakterláncok bináris fájlokká alakulnak az APK-fájl generálásakor. Ugyanitt jön létre az ARSC fájl is, amely tartalmazza a program összes összeállított erőforrásának listáját és azok azonosítóit.

## ARSC fájlformátum

Az .arsc kiterjesztésű fájlok bináris fájlok, amelyeket azután hoznak létre, hogy a fordító, például az ANT (Eclipse) vagy a Gradle (AS) lefordítja az Android alkalmazás kódját az [APK](/hu/compression/apk/) fájl létrehozásához. Az APK-fájlt bármilyen archiváló segédprogrammal, például a WinZip segítségével kibonthatja, hogy megtekinthesse a tartalmát, amely a lefordított java osztályfájlok, azaz a classes.dex. Ezeken kívül tartalmazza ezt az ARSC fájlt is, amely metainformációkat tartalmaz a következőkről:

* Az XML csomópontok
* Az attribútumok
* Az erőforrás-azonosítók

Az APK-fájlban lévő erőforrásokra az erőforrás-azonosítók hivatkoznak, míg az attribútumokat a rendszer futás közben egy értékre oldja fel. Az Android aapt eszköz összegyűjti a fájlokban definiált összes erőforrást összeállításkor, és erőforrás-azonosítókat rendel hozzájuk. Az azonosítók hozzárendelése után a lefordított erőforrásokhoz egy R.java fájl jön létre a forráskódból, valamint az resources.arsc fájlból.

## Hivatkozások

* [Bináris erőforrástáblázat szerkezete](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

