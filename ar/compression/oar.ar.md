{
  "date" : "2021-04-08",
  "keywords" :["ملف مجذاف" , "تنسيق ملف مجذاف" , "ما هو ملف مجذاف" , "ملف" , "مثال مجداف" , "امتداد ملف مجذاف" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - تنسيق ملف أرشيف OpenSimulator" ,
  "description":"تعرف على تنسيق ملف OAR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات OAR وفتحها." ,
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-15"
}

## ما هو ملف OAR؟

الملف ذو الامتداد .oar هو ملف أرشيف يستخدمه تطبيق OpenSimulator وهو خادم تطبيق ثلاثي الأبعاد مفتوح المصدر لإنشاء بيئة افتراضية يمكن الوصول إليها من قبل العديد من المستخدمين عبر الشبكة. يوفر تنسيق ملف OAR بيانات الأصول الضرورية المطلوبة لتحميل التضاريس بالكامل وأنسجة الكائنات والمخزونات على نظام مختلف. يحتوي OpenSimulator أيضًا على شبكة تشعبية اختيارية تتيح للمستخدمين زيارة عمليات تثبيت OpenSimulator الأخرى عبر الويب. تحتوي ملفات OAR على تطبيق / مجذاف من نوع MIME على الإنترنت وتحتوي على واحد أو أكثر من الملفات المؤرشفة.


## تنسيق ملف OAR

OAR هي ملفات ثنائية يتم تخزينها في تنسيق ملف أرشيف مضغوط. أحدث إصدار من تنسيق ملف OAR هو [الإصدار 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) الذي يحتوي على تغييرات كبيرة عن [الإصدار 0.8] السابق (http://opensimulator.org/wiki/OAR_Format_0.8). يدعم الإصدار الأخير تخزين مناطق متعددة في OAR واحد ولا يتوافق مع الإصدارات السابقة مع إصدارات OpenSimulator قبل 0.7.5. ملف OAR هو ملف gzipped tar (tar.gz) بتنسيق unix tar الأصلي (وليس USTAR).

## مثال مناطق OAR
يمكن أن تحتوي ملفات AOR على مناطق متعددة. هيكل الأرشيف كالتالي (هذا المثال يحتوي على 4 مناطق):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

يحتوي ملف التحكم في الأرشيف على رقم إصدار رئيسي لتحديد التوافق مع تغييرات التنسيق المستقبلية. يُشار إلى وجود الأصول بتنسيق OAR بواسطة العنصر المنطقي<assets_included> . المعلومات حول المناطق المضمنة موجودة في بيان موجود في ملف التحكم. مثال على Archive.xml على النحو التالي.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## مراجع

* [تنسيق OAR الإصدار 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

