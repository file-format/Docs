{
  "date" : "2021-04-21",
  "keywords": [ "Was ist eine HS-Datei", "Tutorials zu HS", "HS bedeutet", "HS", "HS-Dateien", "Erweiterung", "Format", "HS-Tutorial", ".hs" , "HS-Beispiel", "hs-Dateierweiterung", "wie man eine hs-Datei öffnet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell-Skriptdateiformat",
  "description":"Erfahren Sie, was ein HS-Dateiformat und APIs sind, die HS-Dateien erstellen und öffnen können.",
  "linktitle" :"HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet-Dateiformat

## Was ist eine Java HS-Datei?

Eine Datei mit der Erweiterung .hs in der Programmiersprache Java ist eine Hilfedokumentationsdatei, die vom JavaHelp-System verwendet wird, wenn es von einer Anwendung aktiviert wird. Es definiert das Helpset für die jeweilige installierte Anwendung und besteht aus mehreren Untergruppen als Teil der Systemhilfe für die Anwendung. Das Java-Programm muss in der Lage sein, die Helpset-Datei zu finden, deren Name mit der Erweiterung .hs endet.

## Java-Helpset-Informationen

Eine .hs-Datei kann die folgenden Informationen enthalten.

|Informationen|Beschreibung|
---|---|
|Zuordnungsdatei|Die Zuordnungsdatei wird verwendet, um Themen-IDs mit dem einheitlichen Ressourcen-Locator oder Pfadnamen von Hypertext-Markup-Language-Themendateien zu verknüpfen.|
|Informationen anzeigen|Informationen, die die im Helpset verwendeten Navigatoren beschreiben. Die Qualitätsnavigatoren sind: Inhaltsverzeichnis, Index und Volltextsuche. weitere navigatoren sind der gloss und auch die favoritennavigatoren. Daten zu benutzerdefinierten Navigatoren sind hier weiter beigefügt.|
<html>|Helpset-Titel|Die \<title> ist in der Helpset-Datei (.hs) beschrieben. Dieser Titel erscheint ganz oben in den meisten Fenstern und allen sekundären Fenstern, die in Ihrer Helpset-Datei umrissen sind.| </html>
|Heimat-ID|Der Titel der (Standard-)ID, die angezeigt wird, wenn der Hilfebeobachter gerufen wird, ohne eine ID anzugeben.|
|Präsentation|Die Fenster, in denen die Assistenzthemen angezeigt werden. Dies kann ein modernes Include des Computerprogramms JavaHelp 2 sein, das weiter unten ausführlicher dargestellt wird \<presentation> .|
|Sub-Helpsets|Dieser frei wählbare Bereich bindet andere Helpsets statisch ein, indem er das Tag verwendet. Die von diesem Tag angezeigten Helpsets werden auf natürliche Weise mit dem Helpset kombiniert, das das Tag enthält. Weitere interessante Punkte rund um das Blending finden Sie in Blending Helpsets.|
|Implementierung|Dieses optionale Segment erstellt eine Registrierung, die eine Schlüsselinformationszuordnung bereitstellt, um die HelpBroker-Klasse zu charakterisieren, die innerhalb der HelpSet.createHelpBroker-Methode verwendet werden soll. Darüber hinaus entscheidet die Registrierungsstelle, dass der Stoffbetrachter für eine bestimmte Emulate-Sorte Client wird.|

## Java HS-Dateiformat

Die Java HS-Dateien liegen im XML-Dateiformat vor und basieren auf der vom World Wide Web Consortium (W3C) vorgeschlagenen Extended Markiup Language-Empfehlung [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Dies bedeutet, dass eine Java HS-Datei im menschenlesbaren XML-Dateiformat vorliegt, das in jeder XML-Reader-Anwendung geöffnet werden kann.

### Beispiel für ein Java-HS-Dateiformat

Das Folgende ist ein Beispiel einer Helpset-Datei aus der [Oracle Helpset-Dokumentation] (https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Verweise
* [Oracle Java Helpset-Datei] (https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell-Skriptdateiformat

## Was ist eine HS-Datei?

Eine Datei mit der Erweiterung .hs ist eine Haskell-Skriptdatei, die in [Haskell](https://wiki.haskell.org/Haskell) geschrieben ist, einer fortgeschrittenen, rein funktionalen Open-Source-Programmiersprache. In HS-Dateien geschriebener Code basiert im Gegensatz zu [C](/de/programming/c/), [C++](/de/programming/cpp/) und dergleichen ausschließlich auf Funktionen, die den Prinzipien der schnellen Entwicklung robuster und präziser Software folgen. Haskell bietet integrierte Parallelität und Parallelität zusammen mit umfangreichen APIs, Profilern und Debuggern, um flexible und qualitativ hochwertige Anwendungen zu erstellen.

## HS-Dateiformat

Wie jede Programmiersprache sind HS-Dateien im Klartextformat geschrieben, das für Menschen lesbar ist. Diese können mit allen verfügbaren Textwerkzeugen erstellt, bearbeitet und angezeigt werden. Die .hs-Quellcodedatei wird mit einem Haskell-Compiler kompiliert, wodurch die ausführbare Binärdatei generiert wird.

### Beispiel für ein HS-Dateiformat

Code kann in eine .hs-Datei geschrieben und mit einem Haskell-Compiler wie [GHC](http://haskell.org/ghc) kompiliert werden. Die folgende Codezeile wird als „HelloWorld.hs“ gespeichert, wie im folgenden Beispiel gezeigt.

```
main = putStrLn "Hello, World!"
```

Dies wird mit dem Befehl kompiliert:

```
$ ghc -o hello hello.hs
```
und die resultierende ausführbare Datei kann ausgeführt werden als:

```
$ ./hello
```
Dies druckt das "Hello, World!" Anweisung zur Ausgabe.

## Verweise

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell in 5 einfachen Schritten](https://wiki.haskell.org/Haskell_in_5_steps)

