{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell Script Bestandsformaat",
  "description":"Meer informatie over wat een HS-bestandsindeling is en API's die HS-bestanden kunnen maken en openen.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet-bestandsindeling

## Wat is een Java HS-bestand?

Een bestand met de extensie .hs in de programmeertaal Java is een helpdocumentatiebestand dat door het JavaHelp-systeem wordt gebruikt wanneer het door een toepassing wordt geactiveerd. Het definieert de helpset voor de specifieke geïnstalleerde applicatie en bestaat uit meerdere subsets als onderdeel van de systeemhelp voor de applicatie. Het Java-programma moet het helpset-bestand kunnen vinden waarvan de naam eindigt op de extensie .hs.

## Java Helpset-informatie

Een .hs-bestand kan de volgende informatie bevatten.

|Informatie|Beschrijving|
---|---|
|Mapbestand|Het kaartbestand wordt gebruikt om onderwerp-ID's te koppelen aan de uniforme resourcelocator of padnaam van onderwerpbestanden in hypertext-markuptaal.|
|Bekijk informatie|Informatie die de navigators beschrijft die in de helpset worden gebruikt. de kwaliteitsnavigators zijn: inhoudsopgave, index en zoeken in volledige tekst. verdere navigators zijn de glans en ook de favorieten-navigators. gegevens met betrekking tot aangepaste navigators zijn hier verder ingesloten.|
<html>|Helpset titel|De \<title> wordt beschreven in het helpset-bestand (.hs). Deze titel lijkt het hoogste van de meeste vensters en alle secundaire vensters die in uw helpset-bestand worden beschreven.| </html>
|Home ID|De titel van de (standaard) ID die wordt weergegeven wanneer de assistentiewachter wordt gebeld zonder een ID op te geven.|
|Presentatie|De vensters waarin de hulponderwerpen worden getoond. Dit kan een moderne versie zijn van het JavaHelp 2-computerprogramma dat hieronder in meer detail wordt weergegeven onder \<presentation> .|
|Sub-helpsets|Dit discretionaire gebied omvat statisch andere helpsets door gebruik te maken van de tag. De helpsets die door deze tag worden weergegeven, worden op natuurlijke wijze gecombineerd in de helpset die de tag bevat. Meer aandachtspunten rond blenden zijn te vinden in Blending Helpsets.|
|Implementatie|Dit discretionaire segment maakt een register dat toewijzing van belangrijke informatie geeft om de klasse HelpBroker te karakteriseren om te gebruiken binnen de HelpSet.createHelpBroker-methode. Het register bepaalt bovendien de stofviewer naar de klant voor een bepaalde emulatiesoort.|

## Java HS-bestandsindeling

De Java HS-bestanden zijn in XML-bestandsindeling en zijn gebaseerd op de voorgestelde aanbeveling van het World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Dit betekent dat een Java HS-bestand een voor mensen leesbaar XML-bestandsformaat is dat in elke XML-lezertoepassing kan worden geopend.

### Java HS-bestandsformaat voorbeeld

Het volgende is een voorbeeld van een helpset-bestand uit [Oracle Helpset-documentatie](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Referenties
* [Oracle Java Helpset-bestand](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script Bestandsformaat

## Wat is een HS-bestand?

Een bestand met de extensie .hs is een Haskell Script-bestand dat is geschreven in [Haskell](https://wiki.haskell.org/Haskell), een geavanceerde puur functionele open-source programmeertaal. Code geschreven in HS-bestand is puur gebaseerd op functies, in tegenstelling tot [C](/nl/programming/c/), [C++](/nl/programming/cpp/) en dergelijke, die de principes volgen van snelle ontwikkeling van robuuste en beknopte software. Haskell biedt ingebouwde gelijktijdigheid en parallellisme, samen met uitgebreide API's, profilers en debuggers om flexibele en hoogwaardige toepassingen te produceren.

## HS-bestandsindeling

Zoals elke programmeertaal, zijn HS-bestanden geschreven in platte tekst die voor mensen leesbaar zijn. Deze kunnen worden gemaakt, bewerkt en bekeken met alle beschikbare teksttools. Het .hs-broncodebestand wordt gecompileerd met een Haskell-compiler, waardoor het uitvoerbare binaire bestand wordt gegenereerd.

### Voorbeeld HS-bestandsindeling

Code kan worden geschreven in een .hs-bestand en gecompileerd met een Haskell-compiler zoals [GHC](https://haskell.org/ghc). De volgende regel code wordt opgeslagen als 'HelloWorld.hs', zoals in het volgende voorbeeld wordt getoond.

```
main = putStrLn "Hello, World!"
```

Dit wordt gecompileerd met het commando:

```
$ ghc -o hello hello.hs
```
en het resulterende uitvoerbare bestand kan worden uitgevoerd als:

```
$ ./hello
```
Dit drukt de "Hello, World!" verklaring naar de uitgang.

## Referenties

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell in 5 eenvoudige stappen](https://wiki.haskell.org/Haskell_in_5_steps)

