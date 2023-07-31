{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - ما هو ملف APPX؟" ,
  "description":"تعرف على تنسيق ملف APPX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات APPX وفتحها." ,
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-12-16"
}

## ما هو ملف APPX؟

ملف APPX هو تنسيق ملف حزمة قابل للتوزيع يُستخدم لتوزيع أحد التطبيقات وتثبيته. تم تقديمه مع Windows 8 ليتم نشره على متجر Microsoft Windows. يحتوي على جميع الملفات المطلوبة لتثبيت تطبيق Windows. وتشمل هذه البيانات الوصفية والملفات ومعلومات بيانات الاعتماد. تنسيق ملف الحزم الأكثر حداثة هو MSIX الذي يتم استخدامه حاليًا بشكل أكثر شيوعًا مقارنة بـ APPX.

## تنسيق ملف APPX - مزيد من المعلومات

يتم حفظ ملفات APPX كملفات مضغوطة بتنسيق ملف [ZIP](/ar/compression/zip/). هذا يجعل الحزمة بأكملها كملف أرشيف بحجم ملف أصغر يسهل تحميله إلى متجر Microsoft.

## كيفية عرض الملفات في ملف APPX؟

لعرض المحتويات أو الملفات داخل ملف APPX ، يجب اتباع الخطوات التالية.

1. نظرًا لأنه يتم تخزين ملفات APPX كملفات مضغوطة ZIP ، قم بإعادة تسمية الملف إلى .zip extension
1. استخدم أي أداة فك ضغط مثل 7-Zip أو WinZip أو WinRAR لاستخراج الملفات الموجودة في ملف APPX

## كيفية إنشاء ملف APPX؟

هناك طريقتان يمكن استخدامهما لإنشاء ملفات APPX.

1. استخدام MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) يُستخدم لإنشاء كليهما حزم التطبيقات (.msix أو .appx) وملفات حزمة التطبيقات. msixbundle أو .appxbundle). بالإضافة إلى ذلك ، يمكنه استخراج الملفات من حزمة التطبيق. يتوفر MakeApp.exe مع Windows 10 SDK ويمكن استخدامه من موجه الأوامر.
1. باستخدام Microsoft Visual Studio - عادةً ما يقوم المطورون [بإنشاء ملفات APPX](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) باستخدام Microsoft Visual Studio. بمجرد اكتمال تطوير التطبيق ويكون التطبيق جاهزًا للنشر ، يمكن إنشاء ملف حزمة APPX عن طريق نشره من داخل Visual Studio.

## مراجع

* [إنشاء حزمة MSIX أو حزمة باستخدام MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [إنشاء ملفات APPX باستخدام Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

