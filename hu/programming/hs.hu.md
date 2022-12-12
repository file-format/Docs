{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS – Haskell Script File Format",
  "description":"További információ arról, hogy mi az a HS-fájlformátum és az API-k, amelyek HS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet fájlformátum

## Mi az a Java HS fájl?

A Java programozási nyelvű .hs kiterjesztésű fájl egy súgódokumentációs fájl, amelyet a JavaHelp rendszer használ, amikor egy alkalmazás aktiválja. Meghatározza a súgót az adott telepített alkalmazáshoz, és több részhalmazból áll az alkalmazás rendszersúgójának részeként. A Java programnak meg kell találnia a helpet fájlt, amelynek neve .hs kiterjesztéssel végződik.

## Java Helpset információk

A .hs fájl a következő információkat tartalmazhatja.

|Információ|Leírás|
---|---|
|Térképfájl|A térképfájl a témaazonosítók társítására szolgál a hiperszöveges jelölőnyelvi témafájlok egységes erőforrás-keresőjéhez vagy elérési útnevéhez.|
|Információ megtekintése|Információ, amely leírja a súgóban használt navigátorokat. a minőségi navigátorok a következők: tartalomjegyzék, index és teljes szöveges keresés. további navigátorok közé tartozik a fényes és a kedvenc navigátorok is. Az egyedi navigátorokra vonatkozó adatok itt találhatók tovább.|
<html>|Súgókészlet címe|A \<title> a helpet (.hs) fájlban található. Ez a cím a legtöbb ablak és minden másodlagos ablak közül a legmagasabbnak tűnik a helpset fájlban.| </html>
|Otthoni azonosító|Az (alapértelmezett) azonosító címe, amely akkor jelenik meg, ha az asszisztensfigyelőt azonosító megadása nélkül hívják.|
|Prezentáció|Az ablakok, amelyekben a segítségnyújtási témákat meg lehet jeleníteni. Ez lehet a JavaHelp 2 számítógépes program modern eleme, amely részletesebben az alábbiakban található: \<presentation> .|
|Sub-helpsets|Ez a tetszőleges terület statikusan más súgókészleteket foglal magában a címke használatával. Az ezzel a címkével jelzett súgókészletek természetes módon egyesülnek a címkét tartalmazó helpet-be. A keveréssel kapcsolatos további érdekességek a Keverési súgóban találhatók.|
|Megvalósítás|Ez a diszkrecionális szegmens létrehoz egy olyan nyilvántartást, amely kulcsfontosságú információleképezést ad a HelpBroker osztály jellemzésére, amelyet a HelpSet.createHelpBroker metóduson belül lehet használni. A nyilvántartó dönt továbbá arról, hogy az anyagmegjelenítőtől az ügyfélig egy adott emuláció rendezés esetén

## Java HS fájlformátum

A Java HS fájlok XML fájlformátumúak, és a World Wide Web Consortium (W3C) Extended Markiup Language javasolt ajánlásán alapulnak [PR-xml-971208] (http://www.w3.org/TR/PR-xml- 971208). Ez azt jelenti, hogy a Java HS-fájl ember által olvasható XML-fájlformátumban van, amely bármely XML-olvasó alkalmazásban megnyitható.

### Java HS fájlformátum példa

A következő egy példa egy helpset fájlra az [Oracle Helpset dokumentációjában] (https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## Hivatkozások
* [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script fájlformátum

## Mi az a HS fájl?

A .hs kiterjesztésű fájl egy Haskell Script fájl, amely [Haskell](https://wiki.haskell.org/Haskell) fejlett, tisztán funkcionális nyílt forráskódú programozási nyelven íródott. A HS fájlba írt kód pusztán olyan függvényeken alapul, mint a [C](/hu/programing/c/), a [C++](/hu/programing/cpp/) és hasonlók, amelyek követik a robusztus és tömör szoftverek gyors fejlődésének alapelveit. A Haskell beépített párhuzamosságot és párhuzamosságot biztosít, valamint gazdag API-kat, profilozókat és hibakeresőket a rugalmas és kiváló minőségű alkalmazások előállításához.

## HS fájlformátum

Mint minden programozási nyelv, a HS fájlok egyszerű szöveges formátumban készülnek, amely ember által olvasható. Ezek létrehozhatók, szerkeszthetők és megtekinthetők bármilyen elérhető szöveges eszközzel. A .hs forráskódfájlt egy Haskell fordító fordítja le, amely előállítja a végrehajtható bináris fájlt.

### HS fájlformátum példa

A kód .hs fájlba írható, és egy Haskell fordítóval, például [GHC] (http://haskell.org/ghc) segítségével fordítható le. A következő kódsor `HelloWorld.hs` néven kerül mentésre, ahogy az a következő mintában látható.

```
main = putStrLn "Hello, World!"
```

Ezt a következő paranccsal állítjuk össze:

```
$ ghc -o hello hello.hs
```
és az eredményül kapott végrehajtható fájl a következőképpen futtatható:

```
$ ./hello
```
Ez kinyomtatja a "Hello, World!" nyilatkozatot a kimenetre.

## Hivatkozások

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell 5 egyszerű lépésben](https://wiki.haskell.org/Haskell_in_5_steps)

