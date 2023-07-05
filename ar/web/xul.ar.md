{
  "date" : "2021-05-24",
  "keywords" :["xul" , "ملف" , "امتداد" , "تنسيق الملف" , "امتداد الملف" , "لغة واجهة مستخدم XML"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - ملف لغة واجهة مستخدم XML" ,
  "description":"تعرف على تنسيق ملف XUL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XUL وفتحها." ,
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-24"
}

## ما هو ملف XUL؟

الملف بامتداد .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) يشير إلى لغة واجهة مستخدم XML) هو ملف لغة ترميز يستند إلى [XML](/ar/web/xml/) لـ إنشاء واجهات المستخدم. تم تطويره بواسطة Mozilla للمطورين لإنشاء عناصر واجهة مستخدم رسومية مماثلة للغات الترميز الأخرى المستخدمة لإنشاء صفحات الويب. تم استخدام XUL على نطاق واسع بواسطة Mozilla في متصفح Firefox الخاص بها حيث استخدم قاعدة بيانات Mozilla. يتم تنفيذ عرض XUL باستخدام ملف
[محرك أبو بريص](https://en.wikipedia.org/wiki/Gecko_ (برنامج)). تحتفظ شوكات Firefox مثل Pale Moon و Basilisk و Waterfox بدعم إضافات XUL. يتم تحديد ملفات XUL بنوع MIME: application / vnd.mozilla.xul + xml.

## تنسيق ملف XUL

تتم كتابة ملفات XUL بنص عادي بناءً على تنسيق ملف XML ويتم تقديمها باستخدام محرك Gecko. الأجزاء الثلاثة الرئيسية لبنية XUL هي:

* "المحتوى" - يتضمن ذلك إعلانات النافذة وعناصر واجهة المستخدم الموجودة بداخلها.
* "الجلد" - يتضمن أي أوراق أنماط وصور وملفات أخرى ذات صلة بالموضوع. يتم وصف مظهر النافذة في أوراق الأنماط.
* "الإعدادات المحلية" - يتم تخزين النص المعروض في النافذة بشكل منفصل ويمكن للمستخدمين استخدام مجموعة متعددة من ملفات اللغة.

### مثال XUL

يُنشئ المثال التالي ثلاثة أزرار مكدسة فوق بعضها البعض في اتجاه رأسي.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## مراجع

* [XUL - بواسطة Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [وثائق XUL المؤرشفة - بواسطة Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

