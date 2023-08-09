{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java Manifest File Format",
  "description":"További információ az MF fájlformátumról és az API-król, amelyek MF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az MF fájl?

Az .mf kiterjesztésű fájl egy Java Manifest fájl, amely információkat tartalmaz az egyes [JAR](/hu/programming/jar/) fájlbejegyzésekről. Maga az MF fájl a JAR fájlban található, és tartalmazza az összes kiterjesztést és csomaggal kapcsolatos definíciót. JAR fájlok előállíthatók futtatható fájlként való használatra. Ebben az esetben a mainfest fájl határozza meg az alkalmazás fő osztályát, amely tartalmazza a **`public static void main`** utasítást. A jegyzékfájlok neve MANIFEST.MF, és bármelyik szövegszerkesztővel megnyitható Windows, MacOS és Linux operációs rendszeren.

## Manifest fájlformátum specifikációi

A [Manifest fájlformátum specifikációi](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) az Oracle által elérhetők a JAR fájlformátumokról szóló útmutatójában. A Manifest fájl fő szakaszokból áll, amelyeket az egyes JAR-fájlbejegyzésekhez tartozó szakaszok listája követ. Minden szakasz bizonyos szabályokat és korlátozásokat követ.

### Fő szakaszok

Egy fő rész:

* információkat tartalmaz a JAR fájl biztonságáról és konfigurációjáról
* információkat tartalmaz arról az alkalmazásról vagy kiterjesztésről, amelynek a JAR fájl része
* meghatározza az egyes jegyzékelemek fő attribútumait

**Megjegyzés**: Ebben a szakaszban egyetlen attribútum sem nevezhető "Név"-nek.

### Egyedi szakaszok

Egy külön szakasz különböző attribútumokat határoz meg a JAR-fájlok csomagjaihoz vagy fájljaihoz. Minden szakasznak egy "Név" nevű attribútummal kell kezdődnie, amelynek értéke a fájl relatív elérési útja, vagy az archívumon kívüli adatokra hivatkozó abszolút URL.

### Manifest Specifikációk

|Attitűdök|Leírás|
---|---|
|manifest-fájl|főszakasz újsor *egyéni szakasz|
|főszakasz|verzióinformáció újsor *fő-attribútum|
|version-info|Manifest-Version : version-number|
|verziószám|számjegy+{.számjegy+}*|
|main-attribute|(bármilyen legitim főattribútum) újsor|
|individual-section|Név : érték újsor *perentry-attribute|
|perentry-attribute|(bármilyen legitim perentry attribútum) újsor|
|újsor|CR LF | LF | CR (nem követi LF)|
|számjegy|{0-9}|

## Hivatkozások

* [Oracle – JAR fájlformátum](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR fájlformátum](https://en.wikipedia.org/wiki/JAR_(file_format))

