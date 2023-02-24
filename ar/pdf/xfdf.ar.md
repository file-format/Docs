{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف XFDF - ما هو ملف XFDF؟" ,
  "description":"تعرف على ملف XFDF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XFDF وفتحها." ,
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف XFDF؟

الملف بامتداد .xfdf هو تنسيق بيانات نماذج XML يتم إنشاؤه باستخدام برنامج Adobe Acrobat. مثل [FDF] (/ar/ pdf / fdf /) ، يحتوي XFDF على وصف لعناصر النموذج وقيمها بتنسيق XML. يمكن أن يتضمن هذا أسماء وقيم الحقول النصية في نموذج PDF. يتم حفظ XFDF بتنسيق يمكن قراءته بواسطة الإنسان ويمكن قراءته برمجيًا باستخدام لغات البرمجة مثل C #.

## تنسيق ملف XFDF - مزيد من المعلومات

يتم حفظ ملفات XFDF بتنسيق ملف XML وهو تنسيق عالمي يُستخدم لاستيراد البيانات وتصديرها. يتكون هيكل ملف XFDF من رأس ، متبوعًا بقيم الحقل ، وبيانات العناصر كما هو موضح أدناه.

| العنصر | السمة | المحتوى |
---|---|---|
| \<XFDF> || العنصر الأعلى |
| \<fields> || كافة قيم الحقول لهذا القالب |
|<field (T)> | الاسم | اسم الحقل |
|<value (V)> | قيمة | قيمة الحقل |

## مراجع

* [دعم تنسيق FDF بواسطة Acrobat] (https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources] (https://opensource.adobe.com/dc-acrobat-sdk-docs/)

