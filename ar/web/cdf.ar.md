{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - تنسيق تعريف القناة" ,
  "description" :"تعرف على ما هو ملف CDF و APIs التي يمكنها إنشاء وفتح ملفات CDF." ,
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-08-18"
}

## ما هو ملف CDF؟

الملف ذو الامتداد .cdf هو تنسيق ملف توزيع المعلومات المستند إلى XLM والذي تم استخدامه لنشر التحديثات المتكررة كـ "قنوات". يتم نشر المعلومات من أي خادم ويب ويتم تسليمها تلقائيًا إلى أجهزة الكمبيوتر المزودة ببرامج استقبال متوافقة مثل متصفحات الويب. يشترك المستخدمون في القنوات النشطة ويتم تسليم التحديثات المجدولة إلى سطح المكتب الخاص بهم.
تم استخدام ملفات CDF سابقًا مع تقنيات Microsoft Active Channel و Active Desktop و Smart Offline Favorites.

## تنسيق ملف CDF

يتم حفظ ملفات CDF كملفات XML وهي تنسيق ملف ويب عام لتبادل المعلومات. تنسيق ملف CDF هو تنسيق قديم الآن ولم يتم اعتماده على نطاق واسع. وبالمقارنة مع هذا ، فإن خدمة RSS الخاصة بـ Netscape كانت أكثر شهرة وانتشارًا.

### مثال على تنسيق ملف CDF

ما يلي هو مثال عام لتنسيق ملف CDF.

""
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE = "http: // domain / folder /"
LASTMOD = "1998-11-05T22: 12"
PRECACHE = "نعم"
المستوى = "0">
<TITLE>عنوان القناة</TITLE>
<ABSTRACT>ملخص محتويات القناة.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD = "1998-11-05T22: 12"
    PRECACHE = "نعم"
المستوى = "1">
<TITLE>عنوان الصفحة الثانية</TITLE>
<ABSTRACT>ملخص محتويات الصفحة الثانية.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
""

## مراجع

* [تنسيق تعريف القناة - بواسطة ويكيبيديا] (https://en.wikipedia.org/wiki/Channel_Definition_Format)

