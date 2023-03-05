{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف DDS- ملف صورة سطح DirectDraw" ,
  "description":"تعرف على تنسيق ملف DDS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DDS وفتحها." ,
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2022-04-02"
}

## ما هو ملف DDS؟

ملف DDS هو ملف صورة نقطية يستخدم تنسيق حاوية DirectDraw Surface (DDS). يخزن مواد غير مضغوطة ومضغوطة (DXTn) وينفذ أنواعًا مختلفة لتخزين أنواع مختلفة من البيانات. كما أنه يدعم عدة أنواع مختلفة من البيانات مثل الأنسجة أحادية الطبقة ، والأنسجة ذات الخرائط الصغيرة ، وخرائط المكعب ، وخرائط الحجم ، ومصفوفات النسيج. يتيح ذلك لملفات DDS تخزين نماذج وحدة نسيج ألعاب الفيديو بالإضافة إلى الصور الرقمية وخلفيات سطح مكتب Windows. تم تطوير تنسيق ملف DDS بواسطة Microsoft لاستخدامه مع DirectX SDK.

## تنسيق ملف DDS

يتم حفظ ملفات DDS كملفات ثنائية ويمكن استخدامها مع DirectX SDK. يستخدم قوة DirectX لتطوير تطبيقات العرض في الوقت الفعلي مثل الألعاب ثلاثية الأبعاد.

### تخطيط ملف DDS

قامت Microsoft بتوثيق [تخطيط ملف DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) بالتفصيل. يحتوي ملف DDS الثنائي على المعلومات التالية.

* كلمة DWORD (رقم سحري) تحتوي على قيمة رمز أربعة أحرف "DDS" (0x20534444).
* وصف للبيانات في الملف.

يصف DDS_HEADER البيانات ويصف DDS_PIXELFORMAT تنسيق البكسل. كلاهما يحل محل هياكل DDSURFACeersC2 و DDSCAPS2 و DDPIXELFORMAT DirectDraw 7 المهملة.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

يوضح [دليل البرمجة لتنسيق ملف DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) مزيدًا من التفاصيل الفنية لتنسيق الملف هذا.

## مراجع

* [DDS - بواسطة Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [الدليل التقني لتنسيق ملف ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

