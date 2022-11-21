
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف ADS - تنسيق ملف مواصفات Ada" ,
  "description":"تعرف على ما هو تنسيق ملف ADS باستخدام الأمثلة وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ADS وفتحها." ,
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-10-30"
}

## ما هو ملف ADS؟

ملف ADS هو ملف مواصفات لمشروع برمجة Ada. إنه مشابه لفئة Java ، أو زوج الرأس والتنفيذ في حالة C ++. يتم تخزين المواصفات العامة والخاصة لحزمة Ada في ملف .ads. وبالمقابل يحتوي ملف .adb على التنفيذ أو هيئات Ada. مثل [C ++] (/ar/ البرمجة / cpp /) ، تقدم Ada الفصل بين المواصفات والتطبيقات المستقلة عن OOP.

يمكن فتح ملفات ADS في أي محرر نصوص مثل Microsoft Notepad و Notepad ++ و Atom.

## تنسيق ملف ADS

تكون ملفات ADS بتنسيق ملف نص عادي بسيط ويمكن فتحها / تحريرها باستخدام أي محرر نصوص. يمكن تنظيم حزم Ada في تسلسلات هرمية. يمكن الإعلان عن وحدة فرعية بالطريقة التالية:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## مراجع

* [حزم Ada] (https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

