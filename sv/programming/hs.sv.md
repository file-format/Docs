{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell Script File Format",
  "description":"Läs mer om vad som är ett HS-filformat och API:er som kan skapa och öppna HS-filer.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet File Format

## Vad är en Java HS fil?

En fil med filändelsen .hs i programmeringsspråket Java är en hjälpdokumentationsfil som används av JavaHelp-systemet när den aktiveras av en applikation. Den definierar hjälpmängden för den speciella applikationen som är installerad och består av flera delmängder som en del av systemhjälpen för applikationen. Java-programmet måste kunna hitta hjälpuppsättningsfilen vars namn slutar med tillägget .hs.

## Java Helpset Information

En .hs-fil kan innehålla följande information.

|Information|Beskrivning|
---|---|
|Map File|Kartfilen används för att associera ämnes-ID:n med den enhetliga resurslokaliseraren eller sökvägen för ämnesfiler för hypertextmarkeringsspråk.|
|Visa information|Information som beskriver de navigatörer som används i hjälpsetet. kvalitetsnavigatorerna är: innehållsförteckning, index och fulltextsökning. ytterligare navigatorer inkluderar glansen och även favoritnavigatorerna. data om anpassade navigatorer bifogas här ytterligare.|
<html>|Helpset title|The \<title> beskrivs i helpset-filen (.hs). Den här titeln verkar vara den högsta av det mest fönster och alla sekundära fönster som beskrivs i din hjälpsetfil.| </html>
|Hem-ID|Titeln på det (standard)-ID som visas när assistansvakten anropas utan att ange ett ID.|
|Presentation|Fönstren där assistansobjekten visas. Detta kan vara en modern del av datorprogrammet JavaHelp 2 som skildras mer i detalj nedanför \<presentation> .|
|Sub-helpsets|Detta diskretionära område innehåller statiskt andra hjälpset genom att använda taggen. Hjälpmängderna som visas av denna tagg kombineras naturligt till hjälpuppsättningen som innehåller taggen. Fler sevärdheter kring blandning finns i Blending Helpsets.|
|Implementation|Detta diskretionära segment gör ett register som ger nyckelinformationsmapping för att karakterisera HelpBroker-klassen för att använda inom HelpSet.createHelpBroker-metoden. Registret bestämmer dessutom ämnesvisaren till klienten för en given emuleringssort.|

## Java HS filformat

Java HS-filerna är i XML-filformat och är baserade på World Wide Web Consortium (W3C) Extended Markiup Language föreslagen rekommendation [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Detta innebär att en Java HS-fil är i mänskligt läsbart XML-filformat som kan öppnas i alla XML-läsarapplikationer.

### Exempel på Java HS-filformat

Följande är ett exempel på en hjälpuppsättningsfil från [Oracle Helpset-dokumentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Referenser
* [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script filformat

## Vad är HS fil?

En fil med tillägget .hs är en Haskell Script-fil som är skriven i [Haskell](https://wiki.haskell.org/Haskell), ett avancerat rent funktionellt programmeringsspråk med öppen källkod. Kod skriven i HS-fil är enbart baserad på funktioner, till skillnad från [C](/sv/programming/c/), [C++](/sv/programming/cpp/) och liknande, som följer principerna för snabb utveckling av robust och koncis mjukvara. Haskell tillhandahåller inbyggd samtidighet och parallellitet tillsammans med rika API:er, profilerare och debuggers för att producera flexibla och högkvalitativa applikationer.

## HS filformat

Som alla programmeringsspråk är HS-filer skrivna i vanligt textformat som är läsbara för människor. Dessa kan skapas, redigeras och visas med alla tillgängliga textverktyg. Källkodsfilen .hs kompileras med en Haskell-kompilator som genererar den körbara binära filen.

### Exempel på HS-filformat

Koden kan skrivas i en .hs-fil och kompileras med en Haskell-kompilator som t.ex. [GHC](http://haskell.org/ghc). Följande kodrad sparas som `HelloWorld.hs` som visas i följande exempel.

```
main = putStrLn "Hello, World!"
```

Detta kompileras med kommandot:

```
$ ghc -o hello hello.hs
```
och den resulterande körbara filen kan köras som:

```
$ ./hello
```
Detta trycker "Hello, World!" uttalande till utgången.

## Referenser

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell i 5 enkla steg](https://wiki.haskell.org/Haskell_in_5_steps)

