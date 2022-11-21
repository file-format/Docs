{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف نصوص هاسكل - HS" ,
  "description":"تعرف على ما هو تنسيق ملف HS و APIs التي يمكنها إنشاء ملفات HS وفتحها." ,
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-06-15"
}

# HS - تنسيق ملف Java HelpSet

## ما هو ملف Java HS؟

الملف ذو الامتداد .hs بلغة برمجة Java هو ملف توثيق تعليمات يستخدمه نظام JavaHelp عندما يتم تنشيطه بواسطة أحد التطبيقات. وهي تحدد مجموعة المساعدة للتطبيق المعين المثبت وتتألف من مجموعات فرعية متعددة كجزء من تعليمات النظام الخاصة بالتطبيق. يجب أن يكون برنامج Java قادرًا على العثور على ملف helpset الذي ينتهي اسمه بالملحق .hs.

## معلومات Java Helpset

قد يحتوي ملف .hs على المعلومات التالية.

| المعلومات | الوصف |
---|---|
| ملف الخريطة | يتم استخدام ملف الخريطة لإقران معرفات الموضوع بمحدد موقع المورد الموحد أو اسم مسار ملفات موضوع لغة تمييز النص التشعبي.
| عرض المعلومات | المعلومات التي تصف الملاحين الذين يتم توظيفهم في مجموعة المساعدة. ملاحو الجودة هم: جدول المحتويات ، والفهرس ، والبحث عن النص الكامل. يتضمن الملاحون الآخرون اللمعان وكذلك الملاحون المفضلون. البيانات المتعلقة بالملاحين المخصصة مرفقة هنا أكثر. |
<html>| عنوان المساعدة | The \<title> تم تحديده داخل ملف helpset (.hs). يظهر هذا العنوان في أعلى معظم النوافذ وأي نوافذ ثانوية موضحة في ملف التعليمات الخاص بك. | </html>
| معرف المنزل | عنوان المعرف (الافتراضي) الذي يتم عرضه عند استدعاء مراقب المساعدة بدون الإشارة إلى معرف. |
| عرض تقديمي | النوافذ التي تظهر فيها مواضيع المساعدة. يمكن أن يكون هذا تضمينًا حديثًا لبرنامج الكمبيوتر JavaHelp 2 الذي تم تصويره بمزيد من التفاصيل أسفل \<presentation> . |
| مجموعات المساعدة الفرعية | تتضمن هذه المنطقة التقديرية بشكل ثابت مجموعات مساعدة أخرى من خلال استخدام العلامة. يتم دمج مجموعات المساعدة التي تعرضها هذه العلامة بشكل طبيعي في مجموعة المساعدة التي تحتوي على العلامة. يمكن العثور على المزيد من النقاط المثيرة للاهتمام حول المزج في Blending Helpsets. |
| التنفيذ | يُنشئ هذا المقطع التقديري سجلاً يعطي تعيين المعلومات الأساسية لتوصيف فئة HelpBroker لاستخدامها في أسلوب HelpSet.createHelpBroker. علاوة على ذلك ، يقرر التسجيل عارض المادة للعميل لفرز محاكاة معين

## تنسيق ملف Java HS

ملفات Java HS موجودة في تنسيق ملف XML وتستند إلى التوصية المقترحة لاتحاد شبكة الويب العالمية (W3C) الموسعة لغة Markiup [PR-xml-971208] (http://www.w3.org/TR/PR-xml- 971208). هذا يعني أن ملف Java HS موجود بتنسيق ملف XML يمكن قراءته بواسطة الإنسان ويمكن فتحه في أي تطبيق قارئ XML.

### مثال على تنسيق ملف Java HS

فيما يلي مثال على ملف helpset بدءًا من [وثائق Oracle Helpset] (https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## مراجع
* [Oracle Java Helpset File] (https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - تنسيق ملف نص هاسكل

## ما هو ملف HS؟

الملف بامتداد .hs هو ملف Haskell Script مكتوب بلغة [Haskell] (https://wiki.haskell.org/Haskell) ، وهي لغة برمجة متقدمة مفتوحة المصدر وظيفية بحتة. يعتمد الكود المكتوب في ملف النظام المنسق تمامًا على الوظائف ، على عكس [C] (/ar/ البرمجة / c /) ، [C ++] (/ar/ البرمجة / cpp /) وعلى حد سواء ، والتي تتبع مبادئ التطوير السريع للبرامج القوية والموجزة. توفر Haskell التزامًا مدمجًا وتوازيًا جنبًا إلى جنب مع واجهات برمجة التطبيقات (API) الغنية ومصفحات البيانات ومصححات الأخطاء لإنتاج تطبيقات مرنة وعالية الجودة.

## تنسيق ملف HS

مثل أي لغة برمجة ، تتم كتابة ملفات HS بتنسيق نص عادي يمكن للبشر قراءته. يمكن إنشاؤها وتحريرها وعرضها باستخدام أي أدوات نصية متاحة. يتم تجميع ملف التعليمات البرمجية المصدر .hs باستخدام مترجم Haskell ، مما يؤدي إلى إنشاء الملف الثنائي القابل للتنفيذ.

### مثال تنسيق ملف HS

يمكن كتابة التعليمات البرمجية في ملف .hs وتصنيفها باستخدام مترجم Haskell مثل [GHC] (http://haskell.org/ghc). يتم حفظ السطر التالي من التعليمات البرمجية كـ `HelloWorld.hs` كما هو موضح في النموذج التالي.

```
main = putStrLn "Hello, World!"
```

يتم تجميع هذا باستخدام الأمر:

```
$ ghc -o hello hello.hs
```
والملف الناتج يمكن تشغيله على النحو التالي:

```
$ ./hello
```
هذا يطبع "Hello، World!" بيان الإخراج.

## مراجع

* [هاسكل] (https://wiki.haskell.org/Haskell)
* [هاسكل في 5 خطوات سهلة] (https://wiki.haskell.org/Haskell_in_5_steps)

