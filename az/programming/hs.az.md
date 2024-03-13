{
  "date": "2021-04-21",
  "keywords": [
"HS faylı nədir",
"HS üzrə dərslər",
"HS deməkdir",
"HS",
"HS faylları",
"uzadılması",
"format",
"HS dərsliyi",
".hs",
"HS nümunəsi",
"hs fayl uzantısı",
"hs faylını necə açmaq olar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS - Haskell skript fayl formatı",
  "description": "HS fayl formatının nə olduğu və HS fayllarını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-azs"
}
},
  "lastmod": "2021-06-15"
}

# HS - Java HelpSet Fayl Formatı

## Java HS faylı nədir?

Java proqramlaşdırma dilində .hs uzantısı olan fayl, proqram tərəfindən aktivləşdirildikdə JavaHelp sistemi tərəfindən istifadə edilən yardım sənədi faylıdır. O, quraşdırılmış xüsusi proqram üçün yardım dəstini müəyyən edir və proqram üçün sistem yardımının bir hissəsi kimi çoxsaylı alt dəstlərdən ibarətdir. Java proqramı adı .hs uzantısı ilə bitən yardım dəsti faylını tapa bilməlidir.

## Java Yardım dəsti məlumatı

.hs faylı aşağıdakı məlumatları ehtiva edə bilər.

|Məlumat|Təsvir|
---|---|
|Xəritə Faylı|Xəritə faylı mövzu ID-lərini vahid resurs lokatoru və ya hipermətn işarələmə dili mövzu fayllarının yol adı ilə əlaqələndirmək üçün istifadə olunur.|
|İnformasiyaya Baxın|Yardım dəsti daxilində işləyən naviqatorları təsvir edən məlumat. keyfiyyətli naviqatorlar bunlardır: mündəricat, indeks və tam mətn axtarışı. əlavə naviqatorlara parıltı və həmçinin sevimli naviqatorlar daxildir. xüsusi naviqatorlarla bağlı məlumatlar daha sonra buraya əlavə olunur.|
|Kömək dəstinin başlığı|<title> yardım dəsti (.hs) faylında təsvir edilmişdir. Bu başlıq yardım dəsti faylınızda təsvir edilən ən çox pəncərə və hər hansı ikinci dərəcəli pəncərələrin ən yüksəkində görünür.|
|Home ID|ID göstərilmədən yardım izləyicisi çağırıldıqda göstərilən (defolt) ID-nin başlığı.|
|Təqdimat|Yardım mövzularının göstəriləcəyi pəncərələr. Bu, aşağıda daha ətraflı təsvir edilən JavaHelp 2 kompüter proqramının müasir bir hissəsi ola bilər.<presentation> .|
|Sub-helpsets|Bu ixtiyari sahə teqdən istifadə etməklə digər köməkçi dəstləri statik olaraq birləşdirir. Bu teq tərəfindən göstərilən yardım dəstləri təbii olaraq etiketi ehtiva edən yardım dəstinə birləşdirilir. Qarışdırma ilə bağlı daha çox maraq dairəsini Blending Helpsets-də tapa bilərsiniz.|
|İcrası|Bu ixtiyari seqment HelpSet.createHelpBroker metodu daxilində istifadə etmək üçün HelpBroker sinfini xarakterizə etmək üçün əsas məlumat xəritələrini verən reyestr yaradır. Bundan əlavə, reyestr müəyyən Emulate sort üçün müştəriyə maddə baxıcısını qərar verir.|

## Java HS fayl formatı

Java HS faylları XML fayl formatındadır və Ümumdünya Veb Konsorsiumunun (W3C) Genişləndirilmiş Markiup Dili tərəfindən təklif olunan [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208) tövsiyəsinə əsaslanır. Bu o deməkdir ki, Java HS faylı istənilən XML oxuyucu proqramında açıla bilən insan tərəfindən oxuna bilən XML fayl formatındadır.

### Java HS Fayl Formatının Nümunəsi

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

## İstinadlar
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell skript fayl formatı

## HS faylı nədir?

.hs genişləndirilməsi olan fayl [Haskell](https://wiki.haskell.org/Haskell), təkmil sırf funksional açıq mənbəli proqramlaşdırma dili ilə yazılmış Haskell Skripti faylıdır. HS faylında yazılmış kod [C](/programming/c/), [C++](/programming/cpp/) və buna bənzər funksiyalardan fərqli olaraq, möhkəm və qısa proqram təminatının sürətli inkişafı prinsiplərinə əməl edən sırf funksiyalara əsaslanır. Haskell çevik və yüksək keyfiyyətli proqramlar istehsal etmək üçün zəngin API-lər, profillər və sazlayıcılarla birlikdə daxili paralellik və paralellik təmin edir.

## HS fayl formatı

Hər hansı bir proqramlaşdırma dili kimi, HS faylları da insanların oxuna biləcəyi düz mətn formatında yazılır. Bunlar istənilən mövcud mətn alətləri ilə yaradıla, redaktə edilə və baxıla bilər. .hs mənbə kodu faylı icra edilə bilən ikili faylı yaradan Haskell kompilyatoru ilə tərtib edilir.

### HS Fayl Formatının Nümunəsi

Kod .hs faylında yazıla və [GHC](https://haskell.org/ghc) kimi Haskell kompilyatorundan istifadə etməklə tərtib edilə bilər. Aşağıdakı kod sətri aşağıdakı nümunədə göstərildiyi kimi `HelloWorld.hs` kimi saxlanılır.

```
main = putStrLn "Hello, World!"
```

Bu əmrdən istifadə edərək tərtib edilir:

```
$ ghc -o hello hello.hs
```
və nəticədə icra olunan fayl aşağıdakı kimi işlədilə bilər:

```
$ ./hello
```
Bu, Salam, Dünya! çıxış üçün bəyanat.

## İstinadlar

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [5 asan addımda Haskell](https://wiki.haskell.org/Haskell_in_5_steps)

