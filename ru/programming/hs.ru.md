{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS — формат файла скрипта Haskell",
  "description":"Узнайте, что такое формат файла HS и API, которые могут создавать и открывать файлы HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS — формат файла справки Java

## .Java HS вариант №

Файл с расширением .hs на языке программирования Java представляет собой файл справочной документации, который используется системой JavaHelp, когда он активируется приложением. Он определяет набор справки для конкретного установленного приложения и состоит из нескольких подмножеств как часть системной справки для приложения. Программа Java должна иметь возможность найти файл справки, имя которого заканчивается расширением .hs.

## Информация о наборе помощи Java

Файл .hs может содержать следующую информацию.

|Информация|Описание|
---|---|
|Файл карты|Файл карты используется для связывания идентификаторов тем с унифицированным указателем ресурсов или путевыми именами файлов тем на языке гипертекстовой разметки.|
|Информация о просмотре|Информация, описывающая навигаторов, задействованных в наборе помощи. Навигаторы качества: оглавление, индекс и полнотекстовый поиск. другие навигаторы включают глянец, а также избранные навигаторы. данные о пользовательских навигаторах приложены здесь далее.|
<html>|Заголовок набора справки|The \<title> описан в файле справки (.hs). Этот заголовок кажется самым высоким из большинства окон и любых вторичных окон, описанных в вашем файле справки. | </html>
|Home ID|Заголовок идентификатора (по умолчанию), который отображается, когда наблюдатель за помощью вызывается без указания идентификатора.|
|Презентация|Окна, в которых отображаются темы помощи. Это может быть современная версия компьютерной программы JavaHelp 2, которая более подробно описана ниже под \<presentation> .|
|Вспомогательные наборы|Эта дискреционная область статически включает другие вспомогательные наборы с помощью тега. Наборы подсказок, отображаемые этим тегом, естественным образом объединяются в набор подсказок, содержащий этот тег. Дополнительные сведения о смешивании можно найти в наборах справки по смешиванию.|
|Реализация|Этот дискреционный сегмент создает реестр, который предоставляет сопоставление ключевой информации для характеристики класса HelpBroker для использования в методе HelpSet.createHelpBroker. Реестр, кроме того, выбирает средство просмотра содержимого для клиента для данного вида эмуляции.

## Формат файла Java HS

Файлы Java HS имеют формат файла XML и основаны на предложенной рекомендации Расширенного языка разметки World Wide Web Consortium (W3C) [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Это означает, что файл Java HS имеет удобочитаемый формат файла XML, который можно открыть в любом приложении для чтения XML.

### Пример формата файла Java HS

Ниже приведен пример файла справки из [документации Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## использованная литература
* [Файл справки Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS — формат файла скрипта Haskell

## .HS вариант №

Файл с расширением .hs представляет собой файл сценария Haskell, написанный на [Haskell](https://wiki.haskell.org/Haskell), передовом чисто функциональном языке программирования с открытым исходным кодом. Код, написанный в файле HS, основан исключительно на функциях, в отличие от [C](/ru/programming/c/), [C++](/ru/programming/cpp/) и им подобных, которые следуют принципам быстрой разработки надежного и лаконичного программного обеспечения. Haskell предоставляет встроенные средства параллелизма и параллелизма, а также богатые API, профилировщики и отладчики для создания гибких и высококачественных приложений.

## Формат файла СС

Как и любой язык программирования, файлы HS записываются в формате простого текста, который удобочитаем. Их можно создавать, редактировать и просматривать с помощью любых доступных текстовых инструментов. Файл исходного кода .hs компилируется с помощью компилятора Haskell, создавая исполняемый двоичный файл.

### Пример формата файла HS

Код можно записать в файл .hs и скомпилировать с помощью компилятора Haskell, такого как [GHC](https://haskell.org/ghc). Следующая строка кода сохраняется как HelloWorld.hs, как показано в следующем примере.

```
main = putStrLn "Hello, World!"
```

Это компилируется с помощью команды:

```
$ ghc -o hello hello.hs
```
и полученный исполняемый файл можно запустить как:

```
$ ./hello
```
Это печатает "Hello, World!" заявление на выходе.

## использованная литература

* [Хаскелл](https://wiki.haskell.org/Haskell)
* [Haskell: 5 простых шагов](https://wiki.haskell.org/Haskell_in_5_steps)

