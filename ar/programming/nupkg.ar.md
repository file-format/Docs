{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف NUPKG - ملف حزمة NuGet" ,
  "description":"تعرف على تنسيق ملف NUPKG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات NUPKG وفتحها." ,
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-03-09"
}

## ما هو ملف NUPKG؟

ملف NUPKG هو ملف حزمة يحتوي على كود مصدر ليتم استخدامه بواسطة برنامج NuGet لإنشاء حزم لاستخدامها في مشاريع .NET. يتم تثبيت مكون NuGet Package Manager كجزء من Microsoft Visual Studio لجلب الحزم من الحزم عبر الإنترنت التي تستضيف المستودع. تساعد ملفات NUPKG المطورين في جلب أحدث الحزم من [Nuget.org](https://nuget.org) باستخدام NuGet Package Manager بدلاً من تنزيل حزم التطوير يدويًا وتثبيتها. يتم إنشاء ملفات NUPKG من ملفات NUSPEC ، وعند جلبها ، قم بتثبيت الحزمة على نظام المستخدم.

## تنسيق ملف NUPKG

ملفات NUPKG هي أرشيفات [ZIP](/ar/compression/zip/) تحتوي على المكتبات المحزومة بداخلها. عند التنزيل ، يمكن إعادة تسميته إلى .zip واستخراجه باستخدام أي أدوات مساعدة مضغوطة قياسية مثل WinZIP و 7-Zip و Apple Archive Utility.

## المرجعي

* [Nuget.org](https://nuget.org)
* [Quickstart: تثبيت واستخدام حزمة في Visual Studio (Windows فقط)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- استوديو)
* [كيفية إنشاء حزمة Nuget ونشرها](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)
