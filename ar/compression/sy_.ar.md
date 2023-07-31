{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ File Format - ملف SYS المضغوط" ,
  "description":"تعرف على تنسيق ملف SY_ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SY_ وفتحها." ,
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2022-06-24"
}

## ما هو ملف SY_؟

ملف SY_ هو ملف .sys مضغوط يستخدمه مثبتات البرامج لتقليل حجم ملفات التثبيت المجمعة داخل المثبت. هذا يقلل من الحجم الكلي للمثبت. يمكن توسيع ملفات SY_ باستخدام الأداة المساعدة لسطر أوامر Microsoft Expand التي تقوم بتوسيع ملف واحد أو أكثر من الملفات المضغوطة.

## SY_ تنسيق الملف - مزيد من المعلومات

SY_ يتم حفظ الملفات على القرص كملفات ثنائية مضغوطة. ومع ذلك ، فإن تنسيق الملف الداخلي الخاص بهم غير متاح للجمهور. يمكن لأداة سطر الأوامر Microsoft Expand توسيع ملفات SY_ باستخدام أحد سطور الأوامر التالية.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
عند توسيعها ، يتم تحويل ملفات SY_ إلى ملف [SYS](https://docs.fileformat.com/system/sys/).

ملفات SY_ تشبه ملفات EX_ و DL_.

## مراجع

* [StuffIt - بواسطة Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

