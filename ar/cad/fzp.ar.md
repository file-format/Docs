{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف FZP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات FZP وفتحها." ,
  "title" :"تنسيق ملف FZP - ملف وصف جزء XML" ,
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
} ,
  "lastmod" : "2022-06-20"
}

## ما هو ملف FZP؟

ملف FZP هو ملف XML تم إنشاؤه بواسطة [Fritzing] (https://fritzing.org/) تطبيق النماذج والتصميم الأولي للدوائر الإلكترونية. يحتوي على معلومات حول خصائص الجزء والموصلات والناقلات بتنسيق ملف [XML] (/ar/ web / xml /). لا يمكن استخدام ملفات FPZ بشكل مستقل في Fritzing. بدلاً من ذلك ، يتم استيرادها كجزء من ملف أرشيف FZPZ.

## تنسيق ملف FZP - مزيد من المعلومات

ملفات FZP هي ملفات XML تحتوي على معلومات حول خصائص الجزء والموصلات والناقلات. بالإضافة إلى ذلك ، تحتوي ملفات FZP أيضًا على معلومات حول العنوان والوصف والمؤلف وتاريخ نشر ملف FZP. عند تصدير ملف جزء Fritzing ، ينشئ تطبيق Fritzing أرشيفًا مضغوطًا [FZPZ] (/ar/ compression / fzpz /) يحتوي على ملف FZP وأربعة ملفات [SVG] (/ar/ image / svg /).

[مواصفات تنسيق ملف FZP] (https://github.com/fritzing/fzp/blob/master/docs/README.md) متاحة على Github بواسطة Fritzing.

## مثال على بنية ملف FZP

يحتوي ملف FZP النموذجي على بنية XML التالية.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## مراجع

* [مواصفات تنسيق ملف FZP] (https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [أجزاء جديدة بامتداد fzpz] (https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

