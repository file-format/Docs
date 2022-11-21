{
  "date" : "2019-12-16",
  "keywords" :["OTS", "file", "extension", "file format", "Excel", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف OTS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات OTS وفتحها." ,
  "title" :"OTS - تنسيق ملف قالب جدول بيانات OpenDocument" ,
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
} ,
  "lastmod" : "2021-01-19"
}

## ما هو ملف OTS؟

الملف ذو الامتداد .ots هو ملف OpenDocument Spreadsheet Template الذي تم إنشاؤه باستخدام برنامج تطبيق Calc المضمن في Apache OpenOffice. برنامج تطبيق Calc مشابه لبرنامج Excel المتاح في Microsoft Office. يتم استخدام تنسيق ملف OTS لإنشاء قوالب تحتوي على إعدادات محددة مسبقًا تتعلق بالأنماط والخط والبيانات وتخطيط جدول البيانات والتنسيق. تحتوي ملفات OTF على `mime-type application / vnd.oasis.opendocument.spreadsheet-template`. يمكن استخدام ملفات القوالب هذه كنقطة بداية لإنشاء وحفظ ملفات البيانات الفعلية المحفوظة في [تنسيق ملف ODS] (/ar/ spreadsheet / ods /). يمكن استخدام ملفات OTS مع تطبيقات مثل OpenOffice و LibreOffice.

## تنسيق ملف OTS

يتم حفظ ملفات OTS بتنسيق ملف OpenDocument XML المستند إلى OASIS والذي يتألف من مجموعة من عدة مستندات ثانوية مع حزمة كأرشيف [ZIP] (/ar/ ضغط / مضغوط /). يخزن كل أرشيف مضغوط جزءًا من المستند الكامل ويخزن كل مستند ثانوي جانبًا معينًا من المستند. على سبيل المثال ، يحتوي مستند ثانوي على معلومات النمط ويحتوي مستند ثانوي آخر على محتوى المستند. يحتوي مستند ODF النموذجي على المكونات التالية:

### محتوى OTS.xml

يحتوي ملف content.xml على المحتوى الفعلي للمستند. هذا لا يشمل البيانات الثنائية مثل الصور ، ومع ذلك.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml من تنسيق ملف OTS

يحتوي ملف styles.xml على معلومات التصميم ويستخدم بكثرة في التنسيق والتخطيط. تشمل أنواع الأنماط:

* أنماط الفقرة
* أنماط الصفحة
* أنماط الشخصية
* أنماط الإطار
* أنماط القائمة

### Meta.xml

يحتوي ملف meta.xml على معلومات حول البيانات الوصفية للملف مثل المؤلف وتاريخ آخر تعديل وما إلى ذلك.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### الإعدادات. xml

يتضمن ملف "settings.xml" إعدادات مستوى المستند مثل عامل التكبير / التصغير وموضع المؤشر.

## مراجع ##

* [مواصفات OpenDocument 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/OpenDocument)

