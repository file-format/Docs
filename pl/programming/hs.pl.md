{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - format pliku skryptu Haskella",
  "description":"Dowiedz się, co to jest format pliku HS i interfejsy API, które mogą tworzyć i otwierać pliki HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS — format pliku zestawu pomocy języka Java

## Czym jest plik Java HS?

Plik z rozszerzeniem .hs w języku programowania Java to plik dokumentacji pomocy, który jest używany przez system JavaHelp, gdy jest aktywowany przez aplikację. Definiuje zestaw pomocy dla konkretnej zainstalowanej aplikacji i składa się z wielu podzbiorów jako część pomocy systemowej dla aplikacji. Program Java musi być w stanie znaleźć plik zestawu pomocy, którego nazwa kończy się rozszerzeniem .hs.

## Informacje o zestawie pomocy Java

Plik .hs może zawierać następujące informacje.

|Informacje|Opis|
---|---|
|Plik mapy|Plik mapy służy do kojarzenia identyfikatorów tematów z jednolitym lokalizatorem zasobów lub nazwą ścieżki plików tematów hipertekstowego języka znaczników.|
|Wyświetl informacje|Informacje opisujące nawigatorów zatrudnionych w zestawie pomocy. nawigatorami jakości są: spis treści, indeks i wyszukiwanie pełnotekstowe. dalsze nawigatory obejmują połysk, a także ulubione nawigatory. dane dotyczące niestandardowych nawigatorów znajdują się w dalszej części.|
<html>|Tytuł zestawu pomocy|Tytuł \<title> jest opisany w pliku helpset (.hs). Ten tytuł wydaje się być najwyższy z większości okien i wszystkich okien drugorzędnych opisanych w twoim pliku helpsetu.| </html>
|Identyfikator domu|Tytuł (domyślnego) identyfikatora, który jest wyświetlany, gdy wezwana zostanie pomoc obserwatora bez podawania identyfikatora.|
|Prezentacja|Okna, w których można pokazać tematy pomocy. Może to być współczesna wersja programu komputerowego JavaHelp 2, która jest przedstawiona bardziej szczegółowo poniżej \<presentation> .|
|Podzestawy pomocy|Ten uznaniowy obszar statycznie włącza inne zestawy pomocy za pomocą znacznika. Zestawy pomocy pokazane przez ten znacznik są naturalnie łączone w zestaw pomocy, który zawiera znacznik. Więcej interesujących miejsc dotyczących mieszania można znaleźć w zestawach pomocy Blending.|
|Implementacja|Ten uznaniowy segment tworzy rejestr, który zapewnia mapowanie kluczowych informacji w celu scharakteryzowania klasy HelpBroker do wykorzystania w metodzie HelpSet.createHelpBroker. Rejestr ponadto decyduje, który użytkownik ma być klientem dla danego rodzaju emulacji.|

## Format pliku Java HS

Pliki Java HS są w formacie XML i są oparte na zaleceniach organizacji World Wide Web Consortium (W3C) Extended Markup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Oznacza to, że plik Java HS jest w czytelnym dla człowieka formacie pliku XML, który można otworzyć w dowolnej aplikacji czytnika XML.

### Przykład formatu pliku Java HS

Poniżej znajduje się przykład pliku zestawu pomocy pochodzącego z [dokumentacji zestawu pomocy Oracle](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Bibliografia
* [Plik zestawu pomocy Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS — format pliku skryptu Haskella

## Czym jest plik HS?

Plik z rozszerzeniem .hs to plik skryptu Haskella napisany w [Haskell](https://wiki.haskell.org/Haskell), zaawansowanym czysto funkcjonalnym języku programowania typu open source. Kod napisany w pliku HS jest oparty wyłącznie na funkcjach, w przeciwieństwie do [C](/pl/programming/c/), [C++](/pl/programming/cpp/) i podobnych, które podążają za zasadami szybkiego tworzenia solidnego i zwięzłego oprogramowania. Haskell zapewnia wbudowaną współbieżność i równoległość wraz z bogatymi interfejsami API, profilerami i debuggerami do tworzenia elastycznych i wysokiej jakości aplikacji.

## Format pliku HS

Jak każdy język programowania, pliki HS są zapisywane w formacie zwykłego tekstu, który jest czytelny dla człowieka. Można je tworzyć, edytować i przeglądać za pomocą dowolnych dostępnych narzędzi tekstowych. Plik kodu źródłowego .hs jest kompilowany za pomocą kompilatora Haskell, generując wykonywalny plik binarny.

### Przykład formatu pliku HS

Kod można zapisać w pliku .hs i skompilować przy użyciu kompilatora Haskella, takiego jak [GHC](http://haskell.org/ghc). Poniższy wiersz kodu jest zapisywany jako `HelloWorld.hs`, jak pokazano w poniższym przykładzie.

```
main = putStrLn "Hello, World!"
```

Jest to kompilowane za pomocą polecenia:

```
$ ghc -o hello hello.hs
```
a wynikowy plik wykonywalny można uruchomić jako:

```
$ ./hello
```
Spowoduje to wydrukowanie komunikatu „Witaj, świecie!” oświadczenie na wyjściu.

## Bibliografia

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell w 5 łatwych krokach](https://wiki.haskell.org/Haskell_in_5_steps)

