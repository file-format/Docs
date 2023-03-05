{
  "date" : "2021-08-27",
  "keywords" :["wsh file", "wsh file format", "what is a wsh file", "file", "wsh example", "wsh file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف WSH وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات WSH وفتحها." ,
  "title" :"WSH - ملف Windows Script" ,
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-08-27"
}

## WSH ما ه
يحتوي ملف بامتداد .wsh على خصائص ومعلمات لبرنامج نصي بلغة برمجة معينة مثل VB أو VBS وما إلى ذلك. الحاجة الفعلية لـ WSH هي استخدامها لتخصيص تنفيذ نصوص معينة. يلزم تشغيل WScript أو CScript وكلاهما مضمنان في نظام التشغيل Windows. تم توفير ملفات WSH مبدئيًا على نظام التشغيل Windows 95 على أقراص التثبيت كمكون اختياري قابل للتكوين والتثبيت للوحة التحكم ، ثم كمكون افتراضي لنظام التشغيل Windows 98.

## WSH تنسيق الملف
يمكن استخدام WSH (Windows Script Host) لأغراض مختلفة ، بما في ذلك الإدارة والبرامج النصية لتسجيل الدخول والأتمتة العامة. WSH يؤسس بيئة لتشغيل البرامج النصية. يستدعي محرك البرنامج النصي المناسب ويخصص مجموعة من الخدمات والكائنات للبرنامج النصي للعمل معها. يمكن تشغيل هذه البرامج النصية في وضع واجهة المستخدم الرسومية ، من كائن COM أو وضع سطر الأوامر ، مما يوفر المرونة للمستخدم لكل من البرامج النصية التفاعلية أو غير التفاعلية.

### أمثلة
هذا مثال بسيط للغاية يوضح بعض VBScript الذي يستخدم جذر WSH COM كائن "WScript" لعرض رسالة مع زر "موافق". عندما يتم تشغيل هذا البرنامج النصي ، سيتم استدعاء محرك CScript أو WScript وسيتم إنشاء بيئة وقت التشغيل.

```
WScript.Echo "Hello world"
WScript.Quit
```


## مراجع

* [Windows Script Host - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



