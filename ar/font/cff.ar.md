{
  "date" : "2020-08-20",
  "keywords" :["cff file", "cff file format", "what is a cff file", "file", "cff example", "cff file extension", "extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - تنسيق ملف الخط المضغوط" ,
  "description":"تعرف على تنسيق ملف CFF وواجهات برمجة التطبيقات لإنشاء ملفات CFF وفتحها." ,
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
} ,
  "lastmod" : "2020-10-21"
}

## ما هو ملف CFF؟

الملف ذو الامتداد .cff هو تنسيق خط مضغوط ويُعرف أيضًا باسم PostScript Type 1 أو CIDFont. يعمل CFF كحاوية لتخزين خطوط متعددة معًا في وحدة واحدة تُعرف باسم FontSet. يسمح تصميم خطوط CFF بدمج رمز لغة PostScript الذي يسمح بمرونة إضافية وقابلية للتوسيع للتنسيق للاستخدام مع بيئات الطابعة. يمكن فتح ملفات خط CFF وتحويلها باستخدام واجهات برمجة التطبيقات مثل [Aspose.Font] (https://products.aspose.com/font).

## تنسيق ملف CFF

ملفات CFF هي ملفات ثنائية تحتوي على تخطيط بيانات منظم ، ولها أنواع بيانات محددة ، ورأس ، وتنظيم الصورة الرمزية وقواميس الجدول. يمكن العثور على مزيد من التفاصيل حول هذه في [مواصفات تنسيق الخط المضغوط] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### تخطيط البيانات
تخطيط البيانات لتنسيق ملف CFF كما هو موضح أدناه.

| الإدخال | التعليقات |
---|---|
| رأس | - |
| الاسمINDEX | - |
| أعلى مؤشر DICT | - |
| مؤشر السلسلة | - |
| مؤشر Subr العالمي | - |
| الترميزات - المحارف | - |
| FDSelect | CIDFonts فقط |
| مؤشر CharStrings | لكل خط |
| الخط DICT INDEX | لكل خط ، CIDFonts فقط |
| DICT خاص | لكل خط |
| فهرس فرعي محلي | لكل خط أو DICT لكل خاص لـ CIDFonts |
| إشعارات حقوق النشر والعلامات التجارية | - |

### أنواع البيانات

أنواع بيانات CFF موضحة في الجدول التالي.

| الاسم | النطاق | الوصف |
---|---|---|
| Card8 | 0 –255 | رقم غير موقع 1 بايت |
| بطاقة 16 | 0 - 65535 | رقم 2 بايت غير موقع |
| الإزاحة | يختلف | إزاحة 1 أو 2 أو 3 أو 4 بايت (محدد بواسطة حقل OffSize) |
| OffSize | 1–4 | رقم غير موقع من 1 بايت يحدد حجم حقل أو حقول الإزاحة |
| SID | 0-64999 | معرف سلسلة 2 بايت |

### العنوان

تبدأ البيانات الثنائية برأس له التنسيق الموضح في الجدول التالي.

| النوع | الاسم | الوصف |
---|---|---|
| Card8 | الكبرى | تنسيق الإصدار الرئيسي (بدءًا من 1) |
| Card8 | ثانوي | تنسيق إصدار ثانوي (يبدأ من 0) |
| Card8 | حجم HDr | حجم الرأس (بايت) |
| OffSize | offSize | حجم الإزاحة المطلق (0) |

## مراجع

* [جدول تنسيق الخط المضغوط] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [تنسيق ملف CFF] (https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

