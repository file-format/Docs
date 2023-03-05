{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - ما هو ملف MSIX؟" ,
  "description":"تعرف على ملف MSIX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MSIX وفتحها." ,
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-12-16"
}

## ما هو ملف MSIX؟

ملف MSIX هو تنسيق حزمة تطبيقات Windows يُستخدم لإنشاء التطبيقات وتوزيعها في Windows 10. هذا هو تنسيق ملف الحزمة الحديث مقارنة بـ [APPX](/ar/ البرمجة / appx /) و MSI التي سيتم التخلص منها أخيرًا إلى تنسيق الملف الجديد هذا. يمكن استخدامه لنشر تطبيقات Win32 و WPF و Windows Forms. ملفات MSIX موثوقة وتستهدف تحسين مساحة القرص والشبكة. يستخدم المطورون هذه لتوزيع البرامج على المستخدمين النهائيين من خلال متجر Microsoft (المعروف سابقًا باسم متجر Windows).

## تنسيق ملف MSIX - مزيد من المعلومات

ملفات MSIX هي [ZIP](/ar/ compression / zip /) - مضغوطة ، مع تضمين جميع الملفات داخل الملف المضغوط. بالإضافة إلى الملفات ذات الصلة بالتطبيق ، يحتوي ملف MSIX على ملفات التكوين [.xml](/ar/ web / xml /) التي تحتوي على معلومات تتعلق بتثبيت التطبيق.

## ماذا يوجد داخل حزمة MSIX؟

تتكون حزمة MSIX من الملفات التالية.

* `AppxBlockMap.xml` - يُعرف باسم ملف مخطط كتلة الحزمة ، وهو مستند XML يحتوي على قائمة بملفات التطبيق مع فهارس وتجزئة تشفير لكل كتلة من البيانات المخزنة في الحزمة.
* `AppxManifest.xml` - مستند XML يحتوي على المعلومات المطلوبة لنشر تطبيق MSIX وعرضه وتحديثه. تتضمن هذه المعلومات هوية الحزمة ، واعتماديات الحزمة ، والإمكانيات المطلوبة ، والعناصر المرئية ، ونقاط القابلية للتوسعة.
* `AppxSignature.p7x` - ملف يتم إنشاؤه عند توقيع الحزمة. يجب توقيع جميع حزم MSIX قبل التثبيت. باستخدام AppxBlockmap.xml ، يمكن للمنصة تثبيت الحزمة والتحقق من صحتها.

## مراجع

* [نظرة عامة على MSIX](https://docs.microsoft.com/en-us/windows/msix/overview)
* [إنشاء ملفات APPX باستخدام Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

