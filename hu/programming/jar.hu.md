{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "mi az a jar fájl", "jar fájl megnyitása", "kiterjesztés", "fájl", "jar fájl", "jar fájlformátum", ". jar kiterjesztése"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java archív fájlformátum",
  "description":"További információ a JAR fájlformátumról és az API-król, amelyek JAR fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a JAR fájl?

A .jar kiterjesztésű fájl egy Java archív fájl, amely számos különböző alkalmazáshoz kapcsolódó fájlt tartalmaz egyetlen fájlként. Ezt a fájlformátumot azért hozták létre, hogy csökkentsék a letöltött Java kisalkalmazások böngészőbe történő betöltésének sebességét HTTP-tranzakción keresztül, elkerülve a több HTTP-kapcsolat létrehozását. Egyetlen JAR-fájl tartalmazhat Java osztályfájlokat ([.class](/hu/programing/class/)), [images](/hu/image/) és [hangokat](/hu/audio/). A JAR-fájlon belüli egyes elemeket az alkalmazás fejlesztője digitálisan aláírhatja eredetük hitelesítése érdekében. A JAR-fájlokat rendszeresen használják olyan funkcionális API-k létrehozására, amelyek az adott API-hoz kapcsolódó speciális funkciókat tartalmaznak.

## JAR fájlformátum

A JAR-fájlok a népszerű [ZIP-fájlformátumon](/hu/compression/zip/) alapulnak, amely egyetlen fájlban archiválja az egyes tartalomfájlokat. A JAR fájlformátum támogatja a tömörítést, ami kisebb fájlméretet eredményez a letöltéshez, és így tovább javítja a letöltési időt. Az Oracle [JAR-fájlspecifikációi](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) cikkben részletesen ismertetjük a JAR-fájlok belső specifikációit.

### A Manifest fájl

JAR-fájl létrehozásakor automatikusan létrejön benne egy jegyzékfájl, amely tartalmazza a JAR-fájl tartalmára vonatkozó metaadat-információkat. Ez a fájl a JAR-fájlba csomagolt tartalmat mutatja. Egy tipikus Manifest fájl a következőképpen néz ki, amely a JAR fájlban található mappákat és osztályokat mutatja.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest Specifikációk

A manifeszt specifikációkat az Oracle az alábbiak szerint határozza meg.

`manifest-file`: főszakasz újsor \*individual-section

`main-section`: verzió-információ újsor \*fő-attribútum

`version-info`: Manifest-Version : verziószám

`verziószám` : számjegy+{.számjegy+}*

`main-attribute`: (bármilyen legitim fő attribútum) újsor

`individual-section`: Név : érték újsor \*perentry-attribute

`perentry-attribute`: (bármilyen jogos perentry attribútum) újsor

`új sor` : CR LF | LF | CR (nem követi az LF)

`digit`: {0-9}

### Futtatható JAR

A JAR-fájlok tartalmazhatnak olyan alkalmazást is, amelyet a Java Virtual Machine (JVM) futtathat, hasonlóan a Microsoft Windows operációs rendszer bármely más alkalmazásához. Ebben az esetben a JVM-nek tudnia kell az alkalmazás belépési pontjáról, amely bármely nyilvános static void main metódussal rendelkező osztály. A jegyzékfájl egy ilyen osztályt a „Main-Class” fejléccel azonosít a következő formátumban:

```
Main-Class: com.example.MyClassName
```



## Hivatkozások

* [A JAR-fájl áttekintése](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR fájlformátum](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Ezek%20are%20built%20on%20the,jar%20file%20extension.)

