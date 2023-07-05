{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف HDMP - تنسيق ملف تفريغ Windows Heap" ,
  "description":"تعرف على تنسيق ملف HDMP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات HDMP وفتحها." ,
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2022-08-19"
}

## ما هو ملف HDMP؟

ملف HDMP هو تفريغ ذاكرة غير مضغوط عند تعطل تطبيق أو برنامج بسبب خطأ. تم إنشاؤه فقط بواسطة نظامي التشغيل Windows XP / Vista ويحتوي على تفريغ لحالة التطبيق عند تعطله. نظرًا لكونها غير مضغوطة ، تشغل ملفات HDMP مساحة أكبر على القرص مقارنة بملفات Minidump [MDMP](/ar/system/mdmp/) التي يتم ضغطها لغرض إعداد التقارير.

تتضمن التطبيقات التي يمكن استخدامها ** لفتح ** أو تحليل ملفات HDMP Microsoft Visual Studio مع أدوات تصحيح الأخطاء لنظام Windows.

## تنسيق ملف HDMP

يتم تخزين ملفات HDMP على قرص كملفات ثنائية ولا تقدم أي فائدة إذا تم فتحها بدون التطبيقات المناسبة. تحتوي على بيانات النظام ذات الصلة المسجلة عند حدوث الخطأ.

### الفرق بين تنسيقات ملفات HDMP و MDMP

HDMP هي ملفات تفريغ ذاكرة غير مضغوطة. في المقابل ، MDMP عبارة عن ملفات تفريغ صغيرة يتم ضغطها لتقليل حجم الملف وإرسالها إلى Microsoft للإبلاغ عن المشكلة.

## المرجعي ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

