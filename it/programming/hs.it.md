{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Formato file script Haskell",
  "description":"Scopri cos'è un formato di file HS e le API che possono creare e aprire file HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Formato file Java HelpSet

## Che cos'è un file Java HS?

Un file con estensione .hs nel linguaggio di programmazione Java è un file di documentazione della guida utilizzato dal sistema JavaHelp quando viene attivato da un'applicazione. Definisce l'helpset per la particolare applicazione installata e comprende più sottoinsiemi come parte dell'help di sistema per l'applicazione. Il programma Java deve essere in grado di trovare il file helpset il cui nome termina con l'estensione .hs.

## Informazioni sull'Helpset Java

Un file .hs può contenere le seguenti informazioni.

|Informazioni|Descrizione|
---|---|
|File mappa|Il file mappa viene utilizzato per associare gli ID argomento al localizzatore di risorse uniforme o al nome del percorso dei file argomento del linguaggio di markup ipertestuale.|
|Visualizza informazioni|Informazioni che descrivono i navigatori utilizzati nell'helpset. i navigatori della qualità sono: sommario, indice e ricerca full-text. ulteriori navigatori includono il gloss e anche i navigatori preferiti. qui di seguito sono allegati i dati relativi ai navigatori personalizzati.|
<html>|Titolo della guida|Il \<title> è descritto all'interno del file helpset (.hs). Questo titolo sembra essere il più alto della maggior parte delle finestre e di tutte le finestre secondarie delineate nel file dell'helpset.| </html>
|Home ID|Il titolo dell'ID (predefinito) visualizzato quando viene chiamato l'osservatore dell'assistenza senza indicare un ID.|
|Presentazione|Le finestre in cui mostrare i soggetti dell'assistenza. Questa può essere una moderna inclusione del programma per computer JavaHelp 2 che è raffigurato in modo più dettagliato sotto \<presentation> .|
|Sub-helpsets|Questa area discrezionale incorpora staticamente altri helpset utilizzando il tag. Gli helpset mostrati da questo tag vengono combinati naturalmente nell'helpset che contiene il tag. Ulteriori punti di interesse sulla fusione possono essere trovati in Blending Helpsets.|
|Implementazione|Questo segmento discrezionale crea un registro che fornisce la mappatura delle informazioni chiave per caratterizzare la classe HelpBroker da utilizzare all'interno del metodo HelpSet.createHelpBroker. Il registro inoltre decide il visualizzatore di sostanze al client per un determinato ordinamento Emulate.|

## Formato file Java HS

I file Java HS sono in formato file XML e sono basati sulla raccomandazione proposta dal World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Ciò significa che un file Java HS è in un formato di file XML leggibile dall'uomo che può essere aperto in qualsiasi applicazione di lettura XML.

### Esempio di formato file Java HS

Quello che segue è un esempio di un file di helpset tratto da [Documentazione Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Riferimenti
* [File Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Formato file script Haskell

## Che cos'è un file HS?

Un file con estensione .hs è un file di script Haskell scritto in [Haskell](https://wiki.haskell.org/Haskell), un linguaggio di programmazione open source puramente funzionale. Il codice scritto nel file HS è puramente basato su funzioni, a differenza di [C](/it/programming/c/), [C++](/it/programming/cpp/) e simili, che seguono i principi dello sviluppo rapido di un software robusto e conciso. Haskell fornisce concorrenza e parallelismo integrati insieme a API avanzate, profiler e debugger per produrre applicazioni flessibili e di alta qualità.

## Formato file HS

Come qualsiasi linguaggio di programmazione, i file HS sono scritti in un formato di testo semplice e leggibile dall'uomo. Questi possono essere creati, modificati e visualizzati con qualsiasi strumento di testo disponibile. Il file del codice sorgente .hs viene compilato con un compilatore Haskell, generando il file binario eseguibile.

### Esempio di formato file HS

Il codice può essere scritto in un file .hs e compilato utilizzando un compilatore Haskell come [GHC](https://haskell.org/ghc). La riga di codice seguente viene salvata come "HelloWorld.hs", come illustrato nell'esempio seguente.

```
main = putStrLn "Hello, World!"
```

Questo viene compilato usando il comando:

```
$ ghc -o hello hello.hs
```
e il file eseguibile risultante può essere eseguito come:

```
$ ./hello
```
Questo stampa il messaggio "Hello, World!" dichiarazione all'output.

## Riferimenti

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell in 5 semplici passaggi](https://wiki.haskell.org/Haskell_in_5_steps)

