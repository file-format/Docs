{
  "date": "2021-04-21",
  "keywords": [
"hvad er en HS-fil",
"tutorials om HS",
"HS betyder",
"HS",
"HS filer",
"udvidelse",
"format",
"HS tutorial",
".hs",
"HS eksempel",
"hs filtypenavn",
"hvordan man åbner en hs fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS - Haskell Script filformat",
  "description": "Lær om, hvad et HS-filformat og API'er er, der kan oprette og åbne HS-filer.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-das"
}
},
  "lastmod": "2021-06-15"
}

# HS - Java HelpSet File Format

## Hvad er en Java HS fil?

En fil med filtypenavnet .hs i programmeringssproget Java er en hjælpedokumentationsfil, der bruges af JavaHelp-systemet, når den aktiveres af en applikation. Den definerer hjælpesættet for den bestemte applikation, der er installeret, og består af flere undersæt som en del af systemhjælpen til applikationen. Java-programmet skal kunne finde hjælpesætfilen, hvis navn ender med .hs-filtypen.

## Java Helpset Information

En .hs-fil kan indeholde følgende oplysninger.

|Information|Beskrivelse|
---|---|
|Kortfil|Kortfilen bruges til at knytte emne-id'er til den ensartede ressourcefinder eller stinavnet på emnefiler til hypertekstmarkeringssprog.|
|Se information|Oplysninger, der beskriver de navigatører, der er ansat i hjælpesættet. kvalitetsnavigatorerne er: indholdsfortegnelse, indeks og fuldtekstsøgning. yderligere navigatorer inkluderer glansen og også favoritnavigatorerne. data vedrørende brugerdefinerede navigatorer er vedlagt her yderligere.|
|Hjælptitel|The \<title> er beskrevet i helpset-filen (.hs). Denne titel vises på det højeste af det mest vindue og alle sekundære vinduer, der er skitseret i din helpset-fil.|
|Hjem-ID|Titlen på det (standard)-id, der vises, når der tilkaldes assistancevagt uden at angive et ID.|
|Præsentation|Vinduerne, hvori hjælpeobjekterne vises. Dette kan være en moderne del af JavaHelp 2-computerprogrammet, der er portrætteret mere detaljeret nedenunder \<presentation> .|
|Sub-helpsets|Dette skønsmæssige område inkorporerer statisk andre hjælpesæt ved at bruge tagget. Hjælpesættene, der vises af dette tag, kombineres naturligt i hjælpesættet, der indeholder tagget. Flere interessepunkter omkring blanding kan findes i Blending Helpsets.|
|Implementering|Dette diskretionære segment laver et register, der giver nøgleinformationsmapping til at karakterisere HelpBroker-klassen til at bruge inden for HelpSet.createHelpBroker-metoden. Registret bestemmer desuden stoffremviseren til klienten for en given emuleringssort.|

## Java HS filformat

Java HS-filerne er i XML-filformat og er baseret på den foreslåede anbefaling fra World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Dette betyder, at en Java HS-fil er i et menneskeligt læsbart XML-filformat, der kan åbnes i ethvert XML-læserprogram.

### Eksempel på Java HS-filformat

The following is an example of a helpset file as from [Oracle Helpset documentation](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Referencer
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script filformat

## Hvad er en HS fil?

En fil med filtypenavnet .hs er en Haskell Script-fil, der er skrevet i [Haskell](https://wiki.haskell.org/Haskell), et avanceret rent funktionelt open source-programmeringssprog. Kode skrevet i HS-fil er udelukkende baseret på funktioner, i modsætning til [C](/programming/c/), [C++](/programming/cpp/) og lignende, som følger principperne for hurtig udvikling af robust og kortfattet software. Haskell leverer indbygget samtidighed og parallelitet sammen med rige API'er, profileringsprogrammer og debuggere for at producere fleksible applikationer af høj kvalitet.

## HS filformat

Som ethvert programmeringssprog er HS-filer skrevet i almindeligt tekstformat, der kan læses af mennesker. Disse kan oprettes, redigeres og ses med alle tilgængelige tekstværktøjer. .hs-kildekodefilen er kompileret med en Haskell-kompiler, der genererer den eksekverbare binære fil.

### Eksempel på HS-filformat

Kode kan skrives i en .hs-fil og kompileres ved hjælp af en Haskell-kompiler såsom [GHC](https://haskell.org/ghc). Den følgende kodelinje gemmes som 'HelloWorld.hs' som vist i følgende eksempel.

```
main = putStrLn "Hello, World!"
```

Dette er kompileret ved hjælp af kommandoen:

```
$ ghc -o hello hello.hs
```
og den resulterende eksekverbare fil kan køres som:

```
$ ./hello
```
Dette udskriver Hej, verden! erklæring til output.

## Referencer

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell i 5 nemme trin](https://wiki.haskell.org/Haskell_in_5_steps)

