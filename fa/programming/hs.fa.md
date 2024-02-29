{
  "date": "2021-04-21",
  "keywords": [
"فایل HS چیست",
"آموزش های HS",
"HS یعنی",
"HS",
"فایل های HS",
"افزونه",
"قالب",
"آموزش HS",
"hs",
"مثال HS",
"پسوند فایل hs",
"نحوه باز کردن فایل hs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HS - فرمت فایل اسکریپت Haskell",
  "description": "در مورد فرمت فایل HS و APIهایی که می توانند فایل های HS را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "HS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-fas"
}
},
  "lastmod": "2021-06-15"
}

# HS - فرمت فایل HelpSet جاوا

## فایل جاوا HS چیست؟

یک فایل با پسوند hs در زبان برنامه نویسی جاوا یک فایل مستندات کمکی است که زمانی که توسط یک برنامه فعال می شود توسط سیستم JavaHelp استفاده می شود. مجموعه کمکی را برای برنامه خاص نصب شده تعریف می کند و از زیر مجموعه های متعددی به عنوان بخشی از کمک سیستم برای برنامه تشکیل شده است. برنامه جاوا باید بتواند فایل helpset را پیدا کند که نام آن با پسوند .hs ختم می شود.

## اطلاعات مجموعه راهنمای جاوا

یک فایل hs ممکن است حاوی اطلاعات زیر باشد.

|اطلاعات|توضیحات|
---|---|
|Map File|فایل نقشه برای مرتبط کردن شناسه‌های موضوع با مکان یاب یکسان منبع یا نام مسیر فایل‌های موضوعی زبان نشانه‌گذاری فرامتن استفاده می‌شود.|
|مشاهده اطلاعات|اطلاعاتی که ناوبرهای به کار گرفته شده در مجموعه راهنما را توصیف می کند. ناوبرهای با کیفیت عبارتند از: فهرست مطالب، فهرست، و جستجوی متن کامل. ناوبرهای بیشتر شامل gloss و همچنین ناوبرهای مورد علاقه است. داده های مربوط به ناوبرهای سفارشی در اینجا در ادامه آمده است.|
|عنوان مجموعه راهنما|<title> در فایل helpset (.hs) مشخص شده است. به نظر می رسد این عنوان بالاترین پنجره و هر پنجره ثانویه ای است که در فایل Helpset شما مشخص شده است.|
|شناسه خانه|عنوان شناسه (پیش‌فرض) که هنگام فراخوانی مراقب کمکی بدون نشان دادن شناسه نمایش داده می‌شود.|
|نمایش|پنجره هایی که در آن افراد کمکی نشان داده می شوند. این می تواند یکی از برنامه های کامپیوتری JavaHelp 2 مدرن باشد که با جزئیات بیشتر در زیر \ به تصویر کشیده شده است<presentation> .|
|دستگاه‌های فرعی|این ناحیه اختیاری با استفاده از تگ، مجموعه‌های کمکی دیگری را به صورت ایستا در بر می‌گیرد. مجموعه های کمکی نشان داده شده توسط این برچسب به طور طبیعی در مجموعه کمکی حاوی تگ ترکیب می شوند. نقاط مورد علاقه بیشتر در مورد ترکیب را می توان در مجموعه راهنمای ترکیبی یافت.|
|پیاده سازی|این بخش اختیاری یک رجیستری ایجاد می کند که نگاشت اطلاعات کلیدی را برای مشخص کردن کلاس HelpBroker برای استفاده در روش HelpSet.createHelpBroker می دهد. علاوه بر این، رجیستری برای یک نوع شبیه‌سازی مشخص، بیننده مواد را به مشتری تعیین می‌کند.|

## فرمت فایل جاوا HS

فایل‌های جاوا HS در فرمت فایل XML هستند و بر اساس توصیه پیشنهادی پیشنهادی کنسرسیوم وب جهانی (W3C) به زبان نشانه‌گذاری توسعه‌یافته [PR-xml-971208](https://www.w3.org/TR/PR-xml-971208) هستند. این بدان معنی است که یک فایل Java HS در قالب فایل XML قابل خواندن توسط انسان است که می تواند در هر برنامه XML reader باز شود.

### نمونه فرمت فایل جاوا HS

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

## منابع
 * [Oracle Java Helpset File](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - فرمت فایل اسکریپت Haskell

## فایل HS چیست؟

یک فایل با پسوند .hs یک فایل اسکریپت Haskell است که به زبان [Haskell](https://wiki.haskell.org/Haskell)، یک زبان برنامه نویسی متن باز و کاملاً کاربردی پیشرفته، نوشته شده است. کد نوشته شده در فایل HS صرفاً بر اساس توابع است، برخلاف [C](/programming/c/)، [C++](/programming/cpp/) و مانند آنها، که از اصول توسعه سریع نرم افزار قوی و مختصر پیروی می کند. Haskell همزمانی و موازی سازی داخلی را همراه با API های غنی، پروفایلرها و اشکال زداها برای تولید برنامه های کاربردی انعطاف پذیر و با کیفیت بالا فراهم می کند.

## فرمت فایل HS

مانند هر زبان برنامه نویسی، فایل های HS در قالب متن ساده نوشته می شوند که برای انسان قابل خواندن هستند. اینها را می توان با هر ابزار متنی موجود ایجاد، ویرایش و مشاهده کرد. فایل کد منبع .hs با یک کامپایلر Haskell کامپایل می شود و فایل باینری قابل اجرا را تولید می کند.

### نمونه فرمت فایل HS

کد را می توان در یک فایل hs نوشت و با استفاده از کامپایلر Haskell مانند [GHC](https://haskell.org/ghc) کامپایل کرد. خط کد زیر به عنوان «HelloWorld.hs» ذخیره می شود که در نمونه زیر نشان داده شده است.

```
main = putStrLn "Hello, World!"
```

این با استفاده از دستور کامپایل شده است:

```
$ ghc -o hello hello.hs
```
و فایل اجرایی حاصل می تواند به صورت زیر اجرا شود:

```
$ ./hello
```
این سلام، جهان! بیانیه به خروجی

## منابع

 * [Haskell](https://wiki.haskell.org/Haskell)
 * [Haskell در 5 مرحله آسان](https://wiki.haskell.org/Haskell_in_5_steps)

