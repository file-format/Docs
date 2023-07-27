{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell Komut Dosyası Dosya Biçimi",
  "description":"HS dosya biçiminin ne olduğu ve HS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Java HelpSet Dosya Biçimi

## Java HS dosyası nedir?

Java programlama dilinde .hs uzantılı bir dosya, bir uygulama tarafından etkinleştirildiğinde JavaHelp sistemi tarafından kullanılan bir yardım dokümantasyon dosyasıdır. Yüklenen belirli uygulama için yardım setini tanımlar ve uygulama için sistem yardımının bir parçası olarak birden çok alt kümeden oluşur. Java programı, adı .hs uzantılı yardım seti dosyasını bulabilmelidir.

## Java Yardım Seti Bilgileri

Bir .hs dosyası aşağıdaki bilgileri içerebilir.

|Bilgi|Açıklama|
---|---|
|Harita Dosyası|Harita dosyası, konu kimliklerini tek tip kaynak bulucu veya köprü metni biçimlendirme dili konu dosyalarının yol adıyla ilişkilendirmek için kullanılır.|
|Bilgi Görüntüle|Yardım setinde kullanılan gezginleri açıklayan bilgiler. kaliteli gezginler şunlardır: içindekiler tablosu, dizin ve tam metin arama. diğer gezginler, parlaklığı ve ayrıca favori gezginleri içerir. özel gezginlerle ilgili veriler burada ayrıca eklenmiştir.|
<html>|Yardım seti başlığı|\<title> yardım seti (.hs) dosyasında özetlenmiştir. Bu başlık, yardım seti dosyanızda özetlenen çoğu pencerenin ve tüm ikincil pencerelerin en üstünde görünür.| </html>
|Ev Kimliği|Yardım izleyici arandığında kimlik belirtilmeden görüntülenen (varsayılan) kimliğin başlığı.|
|Sunum|Yardım konularının gösterileceği pencereler. Bu, altında daha ayrıntılı olarak gösterilen JavaHelp 2 bilgisayar programının modern bir sürümü olabilir.<presentation> .|
|Alt yardım setleri|Bu isteğe bağlı alan, etiketi kullanarak diğer yardım setlerini statik olarak birleştirir. Bu etiket tarafından gösterilen yardım setleri, etiketi içeren yardım setinde doğal olarak birleştirilir. Karıştırma ile ilgili daha fazla ilgi noktası, Karıştırma Yardım Setlerinde bulunabilir.|
|Uygulama|Bu isteğe bağlı bölüm, HelpSet.createHelpBroker yönteminde kullanılacak HelpBroker sınıfını karakterize etmek için anahtar bilgi eşlemesi sağlayan bir kayıt defteri oluşturur. Kayıt ayrıca, madde görüntüleyicinin belirli bir Taklit sıralaması için müşteriye karar verir.|

## Java HS Dosya Biçimi

Java HS dosyaları XML dosya biçimindedir ve World Wide Web Konsorsiyumu (W3C) Genişletilmiş İşaretleme Dili tarafından önerilen tavsiyeye dayalıdır [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208). Bu, bir Java HS dosyasının, herhangi bir XML okuyucu uygulamasında açılabilen, insanlar tarafından okunabilen XML dosyası biçiminde olduğu anlamına gelir.

### Java HS Dosya Biçimi Örneği

Aşağıda, [Oracle Yardım Seti belgeleri](https://docs.Oracle.com/cd/E19253-01/819-0913/yazar/helpset.html)'den bir yardım seti dosyası örneği verilmiştir.

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

## Referanslar
* [Oracle Java Yardım Kümesi Dosyası](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Haskell Komut Dosyası Dosya Biçimi

## HS dosyası nedir?

.hs uzantılı bir dosya, tamamen işlevsel gelişmiş bir açık kaynak programlama dili olan [Haskell](https://wiki.haskell.org/Haskell) ile yazılmış bir Haskell Komut Dosyası dosyasıdır. HS dosyasında yazılan kod, [C](/tr/programming/c/), [C++](/tr/programming/cpp/) ve benzerlerinden farklı olarak, sağlam ve özlü yazılımın hızlı geliştirme ilkelerini izleyen tamamen işlevlere dayalıdır. Haskell, esnek ve yüksek kaliteli uygulamalar üretmek için zengin API'ler, profil oluşturucular ve hata ayıklayıcılarla birlikte yerleşik eşzamanlılık ve paralellik sağlar.

## HS Dosya Biçimi

Herhangi bir programlama dili gibi, HS dosyaları da insan tarafından okunabilen düz metin biçiminde yazılır. Bunlar, mevcut herhangi bir metin aracıyla oluşturulabilir, düzenlenebilir ve görüntülenebilir. .hs kaynak kodu dosyası, yürütülebilir ikili dosyayı oluşturan bir Haskell derleyicisiyle derlenir.

### HS Dosya Biçimi Örneği

Kod bir .hs dosyasına yazılabilir ve [GHC](https://haskell.org/ghc) gibi bir Haskell derleyici kullanılarak derlenebilir. Aşağıdaki kod satırı, aşağıdaki örnekte gösterildiği gibi 'HelloWorld.hs' olarak kaydedilir.

```
main = putStrLn "Hello, World!"
```

Bu, şu komut kullanılarak derlenir:

```
$ ghc -o hello hello.hs
```
ve ortaya çıkan yürütülebilir dosya şu şekilde çalıştırılabilir:

```
$ ./hello
```
Bu, "Merhaba Dünya!" çıkış için ifade.

## Referanslar

* [Haskell](https://wiki.haskell.org/Haskell)
* [5 Kolay Adımda Haskell](https://wiki.haskell.org/Haskell_in_5_steps)

