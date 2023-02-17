{
  "date" : "2021-08-31",
  "keywords" :["ملف xbe" , "تنسيق ملف xbe" , "ما هو ملف xbe" , "ملف" , "xbe example" , "امتداد ملف xbe" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف XBE وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XBE وفتحها." ,
  "title" :"XBE - ملف حزمة تطبيق iOS" ,
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-08-31"
}

## ما هو ملف XBE؟
الملف الذي يحتوي على ملحق .xbe هو تطبيق قابل للتنفيذ من قرص لعبة فيديو Xbox. ملفات XBE هي الملفات الرئيسية التي يتم تنفيذها في نظام Xbox ولا يُفترض فتحها عادةً على جهاز كمبيوتر ، ولكن يمكن فتحها على جهاز كمبيوتر باستخدام برنامج محاكاة Xbox. عادةً ما يتم إنشاء هذه الملفات بواسطة مطوري الألعاب ، ثم يتم توقيعها بواسطة Microsoft. يشبه هيكل الملف ملفات Windows PE ، ولكن يتم تطبيق بعض التغييرات المهمة وفقًا لإعدادات XBox لجعله قابلاً للتشغيل في XBox.

## تنسيق ملف XBE
يتكون ملف XBE من رأس الصورة ، ومجموعة من رؤوس الأقسام ، وشهادة ، وبيانات التخزين المحلي لمؤشر الترابط ، ومجموعة من إصدارات المكتبة ، والصورة النقطية لـ Microsoft ، والأقسام التي تحتوي على التعليمات البرمجية والموارد.

### رأس الصورة
يشتمل رأس الصورة على المعلومات التي تشرح مكان وجود المكونات الأخرى للملف التنفيذي داخل الملف ، وكيف يجب معالجة الملف القابل للتشغيل وتحميله.

### جدول TLS
يتكون جدول TLS من جميع المعلومات التي يحتاجها XBE لإعداد التخزين المحلي لمؤشر الترابط بشكل صحيح. إنه فريد بشكل أساسي لدليل TLS الموجود في ملفات PE32 ، ويمكن نسخه مباشرة من هناك. قد يتم حذف هذا الجدول ، إذا كان ملف XBE لا يستخدم أي تخزين محلي لمؤشر الترابط ، والحقل المعني في رأس الصورة مضبوط على الصفر.

| الأوفست | الحجم | الاسم | الوصف |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | بدء البيانات الأولية | العنوان المطلق (أي ليس RVA) لبداية بيانات متغير TLS في صورة البرنامج. |
| 0x0004 | 0x0004 | نهاية البيانات الخام | عنوان مطلق (أي ليس RVA) لنهاية بيانات متغير TLS في صورة البرنامج. |
| 0x0008 | 0x0004 | عنوان الفهرس | العنوان المطلق (أي ليس RVA) لمتغير فهرس TLS. |
| 0x000C | 0x0004 | عنوان الاسترجاعات | العنوان المطلق (أي ليس RVA) لجدول وظائف رد الاتصال TLS المنتهية خالية. |
| 0x0010 | 0x0004 | حجم ملء الصفر | عدد البايتات التي تلي البيانات الأولية التي يجب تعيينها على صفر في الذاكرة. |
| 0x0014 | 0x0004 | الخصائص | يصف المحاذاة. |

### شهادة

الشهادة إلزامية لكل ملف Xbox قابل للتنفيذ يحتوي على معلومات حول العناوين:
 


- وقت وتاريخ إنشاء الشهادة
- معرف العنوان
- اسم العنوان
- معرفات العنوان البديلة
- أنواع الوسائط المسموح بها التي يمكن تشغيل الملف التنفيذي منها (HD ، DVD ، CD ، إلخ.)
- منطقة اللعبة
- تقييمات اللعبة
- رقم القرص
- إصدار
- البيانات الأولية لمفتاح LAN المستخدمة في ارتباط النظام
- بيانات خام مفتاح التوقيع (تستخدم لتوقيع savegames)
- مفاتيح التوقيع البديلة
- الحجم الأصلي للشهادة
- اسم الخدمة عبر الإنترنت (غير موجود في الملفات التنفيذية المبكرة)
- أعلام أمان وقت التشغيل (غير موجودة في الملفات التنفيذية المبكرة)
 


### أنواع الوسائط المسموح بها
أنواع الوسائط التي يسمح الملف التنفيذي بتشغيلها منها. القيم التالية معروفة:
| نوع الوسائط | القيمة |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| قرص مضغوط | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| دونغل | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### الأقسام
يتم التعبير عن الأقسام بواسطة رؤوس الأقسام. تبدأ رؤوس الأقسام مباشرة بعد الشهادة وتحتوي على معلومات حيث توجد الأقسام الفعلية في الملف. يوجد دائمًا قسمان على الأقل في ملف تنفيذي لـ Xbox:


- .نص


- .rdata


## مراجع



* [Xbe - XBox قابل للتنفيذ] (https://xboxdevwiki.net/Xbe)

