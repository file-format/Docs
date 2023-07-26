{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS – Файлов формат на Haskell скрипт",
  "description":"Научете какво е HS файлов формат и API, които могат да създават и отварят HS файлове.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet файлов формат

## Какво е Java HS файл?

Файл с разширение .hs на езика за програмиране Java е файл с помощна документация, който се използва от системата JavaHelp, когато се активира от приложение. Той дефинира помощния набор за конкретното инсталирано приложение и се състои от множество подмножества като част от системната помощ за приложението. Програмата Java трябва да може да намери файла с помощна програма, чието име завършва с разширението .hs.

## Информация за Java Helpset

Файлът .hs може да съдържа следната информация.

|Информация|Описание|
---|---|
|Картографски файл|Картографският файл се използва за свързване на идентификатори на теми с унифицирания локатор на ресурси или името на пътя на файловете с теми на езика за маркиране на хипертекст.|
|Преглед на информация|Информация, която описва навигаторите, използвани в набора за помощ. качествените навигатори са: съдържание, индекс и търсене в пълен текст. Допълнителните навигатори включват гланц, а също и любимите навигатори. данните относно персонализираните навигатори са приложени тук допълнително.|
<html>|Заглавие на набора за помощ|The \<title> е очертан във файла helpset (.hs). Това заглавие изглежда най-високо от най-прозорците и всички второстепенни прозорци, очертани във вашия помощен файл.| </html>
|Home ID|Заглавието на (по подразбиране) ID, което се показва, когато помощният наблюдател е извикан без посочване на ID.|
|Презентация|Прозорците, в които да се показват помощните теми. Това може да бъде модерно включване на компютърната програма JavaHelp 2, което е описано по-подробно под \<presentation> .|
|Подпомощни набори|Тази дискреционна област статично включва други помощни набори чрез използване на етикета. Помощните набори, показани от този етикет, се комбинират естествено в помощния набор, който съдържа маркера. Още точки на интерес около смесването могат да бъдат намерени в Помощни набори за смесване.|
|Внедряване|Този дискреционен сегмент прави регистър, който дава съпоставяне на ключова информация за характеризиране на класа HelpBroker за използване в рамките на метода HelpSet.createHelpBroker. Регистърът освен това решава коя програма за разглеждане на субстанции е клиент за дадено сортиране на Emulate.|

## Java HS файлов формат

Java HS файловете са в XML файлов формат и са базирани на предложената препоръка на World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Това означава, че Java HS файл е в четим от хора XML файлов формат, който може да бъде отворен във всяко приложение за четене на XML.

### Пример за файлов формат на Java HS

По-долу е пример за файл с набор за помощ от [документация на набора за помощ на Oracle](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Препратки
* [файл за Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Файлов формат на Haskell скрипт

## Какво е HS файл?

Файл с разширение .hs е файл на Haskell Script, който е написан на [Haskell](https://wiki.haskell.org/Haskell), усъвършенстван чисто функционален език за програмиране с отворен код. Кодът, написан в HS файл, се основава изцяло на функции, за разлика от [C](/bg/programming/c/), [C++](/bg/programming/cpp/) и други подобни, които следват принципите за бързо разработване на стабилен и кратък софтуер. Haskell осигурява вградена паралелност и паралелизъм заедно с богати API, програми за профилиране и отстраняване на грешки за създаване на гъвкави и висококачествени приложения.

## HS файлов формат

Както всеки език за програмиране, HS файловете са написани в обикновен текстов формат, който е четим от хора. Те могат да се създават, редактират и преглеждат с всички налични текстови инструменти. Файлът с изходен код .hs се компилира с компилатор Haskell, генерирайки изпълнимия двоичен файл.

### Пример за HS файлов формат

Кодът може да бъде написан в .hs файл и компилиран с помощта на компилатор на Haskell като [GHC](https://haskell.org/ghc). Следният ред от код се записва като „HelloWorld.hs“, както е показано в следния пример.

```
main = putStrLn "Hello, World!"
```

Това се компилира с помощта на командата:

```
$ ghc -o hello hello.hs
```
и полученият изпълним файл може да се изпълнява като:

```
$ ./hello
```
Това отпечатва "Hello, World!" изявление към изхода.

## Препратки

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell в 5 лесни стъпки](https://wiki.haskell.org/Haskell_in_5_steps)

