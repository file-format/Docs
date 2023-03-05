{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell Script File Format",
  "description":"Zjistěte, co je formát souboru HS a rozhraní API, která mohou vytvářet a otevírat soubory HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Formát souborů Java HelpSet

## Co je soubor Java HS?

Soubor s příponou .hs v programovacím jazyce Java je soubor dokumentace nápovědy, který používá systém JavaHelp, když je aktivován aplikací. Definuje nápovědu pro konkrétní nainstalovanou aplikaci a obsahuje více podmnožin jako součást systémové nápovědy k aplikaci. Java program musí být schopen najít soubor nápovědy, jehož název končí příponou .hs.

## Informace o nápovědě Java

Soubor .hs může obsahovat následující informace.

|Informace|Popis|
---|---|
|Mapový soubor|Mapový soubor se používá ke spojení ID témat s jednotným lokátorem zdrojů nebo názvem cesty k tematickým souborům v jazyce hypertextu.|
|Zobrazit informace|Informace, které popisují navigátory používané v sadě nápovědy. kvalitními navigátory jsou: obsah, rejstřík a fulltextové vyhledávání. mezi další navigátory patří lesk a také oblíbené navigátory. údaje týkající se uživatelských navigátorů jsou zde dále přiloženy.|
<html>|Název sady nápovědy|\<title> je popsána v souboru helpset (.hs). Tento nadpis se zdá být v nejvyšším z nejvíce oken a všech sekundárních oken uvedených v souboru nápovědy.| </html>
|Home ID|Název (výchozího) ID, které se zobrazí při volání asistenčního pozorovatele bez uvedení ID.|
|Prezentace|Okna, ve kterých se zobrazují asistenční předměty. To může být moderní zahrnutí počítačového programu JavaHelp 2, který je podrobněji zobrazen pod \<presentation> .|
|Podřazené sady nápovědy|Tato volitelná oblast staticky zahrnuje další sady nápovědy pomocí značky. Sady nápovědy zobrazené touto značkou jsou přirozeně spojeny do sady nápovědy, která značku obsahuje. Další zajímavosti týkající se prolnutí naleznete v Nápovědách pro prolínání.|
|Implementace|Tento volitelný segment vytváří registr, který poskytuje mapování klíčových informací pro charakterizaci třídy HelpBroker k použití v rámci metody HelpSet.createHelpBroker. Registr navíc určuje prohlížeč látek klientovi pro daný druh emulace.|

## Formát souborů Java HS

Soubory Java HS jsou ve formátu XML a jsou založeny na doporučení navrženém konsorciem World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). To znamená, že soubor Java HS je ve formátu souboru XML čitelném pro člověka, který lze otevřít v jakékoli aplikaci pro čtení XML.

### Příklad formátu souboru Java HS

Níže je uveden příklad souboru nápovědy z [dokumentace sady nápovědy Oracle](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Reference
* [Soubor Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Script File Format

## Co je soubor HS?

Soubor s příponou .hs je soubor Haskell Script, který je napsán v [Haskell](https://wiki.haskell.org/Haskell), pokročilém čistě funkčním open-source programovacím jazyce. Kód napsaný v HS souboru je založen čistě na funkcích, na rozdíl od [C](/cs/programming/c/), [C++](/cs/programming/cpp/) a podobně, které se řídí principy rychlého vývoje robustního a stručného softwaru. Haskell poskytuje vestavěnou souběžnost a paralelismus spolu s bohatými API, profilery a debuggery pro vytváření flexibilních a vysoce kvalitních aplikací.

## Formát souboru HS

Jako každý programovací jazyk jsou soubory HS psány ve formátu prostého textu, který je čitelný pro člověka. Ty lze vytvářet, upravovat a prohlížet pomocí jakýchkoli dostupných textových nástrojů. Soubor zdrojového kódu .hs je zkompilován pomocí kompilátoru Haskell, který generuje spustitelný binární soubor.

### Příklad formátu souboru HS

Kód lze zapsat do souboru .hs a zkompilovat pomocí kompilátoru Haskell, jako je [GHC](http://haskell.org/ghc). Následující řádek kódu je uložen jako „HelloWorld.hs“, jak je znázorněno v následující ukázce.

```
main = putStrLn "Hello, World!"
```

To se zkompiluje pomocí příkazu:

```
$ ghc -o hello hello.hs
```
a výsledný spustitelný soubor lze spustit jako:

```
$ ./hello
```
Tím se vytiskne nápis "Ahoj, světe!" prohlášení k výstupu.

## Reference

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell v 5 snadných krocích](https://wiki.haskell.org/Haskell_in_5_steps)

