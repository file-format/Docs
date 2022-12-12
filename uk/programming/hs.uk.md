{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - формат файлу сценарію Haskell",
  "description":"Дізнайтеся, що таке формат файлу HS та API, які можуть створювати та відкривати файли HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Формат файлу Java HelpSet

## Що таке файл Java HS?

Файл із розширенням .hs мовою програмування Java — це файл довідкової документації, який використовується системою JavaHelp, коли її активує програма. Він визначає набір довідки для конкретної встановленої програми та складається з кількох піднаборів як частину системної довідки для програми. Програма Java повинна мати можливість знайти файл довідки, ім’я якого закінчується розширенням .hs.

## Інформація про набір довідок Java

Файл .hs може містити таку інформацію.

|Інформація|Опис|
---|---|
|Мап-файл|Мап-файл використовується для зв'язування ідентифікаторів тем з уніфікованим покажчиком ресурсу або іменем шляху файлів тем мови гіпертекстової розмітки.|
|Переглянути інформацію|Інформація, що описує навігатори, які використовуються в наборі допомоги. навігаторами якості є: зміст, покажчик і повнотекстовий пошук. інші навігатори включають глянець, а також навігатори вибраного. дані щодо користувальницьких навігаторів додаються тут далі.|
<html>|Назва довідкової системи|The \<title> описано у файлі довідки (.hs). Цей заголовок виглядає найвищим із вікон і будь-яких додаткових вікон, окреслених у вашому файлі довідки.| </html>
|Home ID|Назва ідентифікатора (за замовчуванням), який відображається під час виклику спостерігача без вказівки ідентифікатора.|
|Презентація|Вікна, у яких відображаються предмети допомоги. Це може бути сучасна частина комп’ютерної програми JavaHelp 2, яка більш детально зображена нижче \<presentation> .|
|Піднабори довідок|Ця дискреційна область статично включає інші набори довідок за допомогою тегу. Довідкові набори, показані цим тегом, об’єднуються природним чином у довідковий набір, який містить тег. Більше цікавих місць щодо змішування можна знайти в наборах довідок для змішування.|
|Реалізація|Цей дискреційний сегмент створює реєстр, який надає відображення ключової інформації для характеристики класу HelpBroker для використання в методі HelpSet.createHelpBroker. Крім того, реєстр вирішує переглядач субстанції для клієнта для заданого сортування Emulate.|

## Формат файлу Java HS

Файли Java HS мають формат файлу XML і базуються на запропонованій рекомендації Консорціуму всесвітньої павутини (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Це означає, що файл Java HS має читабельний формат XML-файлу, який можна відкрити в будь-якій програмі для читання XML.

### Приклад формату файлу Java HS

Нижче наведено приклад файлу довідки з [документації Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Список літератури
* [Файл довідки Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - формат файлу сценарію Haskell

## Що таке файл HS?

Файл із розширенням .hs — це файл сценарію Haskell, написаний мовою [Haskell](https://wiki.haskell.org/Haskell), вдосконаленою чисто функціональною мовою програмування з відкритим кодом. Код, написаний у файлі HS, базується виключно на функціях, на відміну від [C](/uk/programming/c/), [C++](/uk/programming/cpp/) тощо, які дотримуються принципів швидкої розробки надійного та лаконічного програмного забезпечення. Haskell забезпечує вбудований паралелізм і паралелізм разом із багатими API, профайлерами та налагоджувачами для створення гнучких і високоякісних програм.

## Формат файлу HS

Як і будь-яка мова програмування, файли HS записуються у форматі звичайного тексту, який легко читається людиною. Їх можна створювати, редагувати та переглядати будь-якими доступними текстовими інструментами. Файл вихідного коду .hs компілюється за допомогою компілятора Haskell, який генерує виконуваний двійковий файл.

### Приклад формату файлу HS

Код можна записати у файлі .hs і скомпільувати за допомогою компілятора Haskell, такого як [GHC](http://haskell.org/ghc). Наступний рядок коду зберігається як `HelloWorld.hs`, як показано в наступному прикладі.

```
main = putStrLn "Hello, World!"
```

Це компілюється за допомогою команди:

```
$ ghc -o hello hello.hs
```
і отриманий виконуваний файл можна запустити як:

```
$ ./hello
```
Це друкує "Hello, World!" оператор на вихід.

## Список літератури

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell за 5 простих кроків](https://wiki.haskell.org/Haskell_in_5_steps)

