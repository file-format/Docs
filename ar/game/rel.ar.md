{
  "date" : "2021-09-08",
  "keywords" :["rel file" , "rel file format" , "what is a rel file" , "file" , "rel example" , "rel file extension" , "extension" , "format"] ,
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف REL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات REL وفتحها." ,
  "title" :"REL - ملف الوحدة القابلة للنقل" ,
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
} ,
  "lastmod" : "2021-09-08"
}

## ما هو ملف REL؟
يمكن استخدام ملف بامتداد .rel لعدة أنواع من الأغراض. لذلك ، من حيث تصنيف اللعبة ، يُعرف باسم ملف وحدة قابلة للنقل تستخدمه بعض ألعاب Nintendo Wii ، مثل Brawl و Super Smash Bros و Mario Kart Wii. وهي تشتمل على بيانات طريقة اللعب ، بما في ذلك نماذج الشخصيات والمراحل. تعمل ملفات REL بشكل مشابه لملفات .DLL التي يستخدمها نظام التشغيل Microsoft Windows.

## تنسيق ملف REL
في تنسيق ملف REL ، يتم تقسيم الملف إلى عدة أقسام ، مجمعة حسب الوصول ، على سبيل المثال قراءة البيانات فقط في قسم واحد ، يتم وضع كل التعليمات البرمجية القابلة للتنفيذ في قسم آخر ، وما إلى ذلك. يبدأ الملف بقسم رأس ، متبوعًا بـ:
- جدول يحتوي على قسم المعلومات.
- بيانات القسم.
- معلومات الانتقال.

### رأس الملف
يبدأ الملف برأس يصل إلى 0x4C بايت:
| الأوفست | الحجم | اسم الحقل | الوصف |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | معرف | رقم التعريف التعسفي. يجب أن يكون فريدًا بين جميع RELs التي تستخدمها اللعبة. يجب ألا يكون 0. |
| 0x04 | 4 | التالي | المؤشر إلى الوحدة التالية ، معبأ في وقت التشغيل. |
| 0x08 | 4 | السابق | المؤشر إلى الوحدة السابقة ، معبأ في وقت التشغيل. |
| 0x0c | 4 | عدد الأقسام | عدد الأقسام في الملف. |
| 0x10 | 4 | sectionInfoOffset | إزاحة إلى بداية جدول القسم. |
| 0x14 | 4 | اسم الإزاحة | الإزاحة إلى سلسلة ASCII التي تحتوي على اسم الوحدة النمطية. قد يكون NULL. نسبي لبداية ملف REL. |
| 0x18 | 4 | الاسمالحجم | حجم اسم الوحدة بالبايت. |
| 0x1c | 4 | الإصدار | رقم إصدار تنسيق ملف REL. |
| 0x20 | 4 | الحجم | حجم قسم ".bss". |
| 0x24 | 4 | relOffset | تعويض إلى جدول النقل. |
| 0x28 | 4 | إمبوفست | الإزاحة إلى جدول عفريت. |
| 0x2c | 4 | إمبسيزي | حجم جدول عفريت بالبايت. |
| 0x30 | 1 | prologSection | فهرس في جدول القسم الذي يرتبط برولوج به. تخطي إذا كان هذا الحقل 0. |
| 0x31 | 1 | قسم الخاتمه | فهرس في جدول القسم الذي تتعلق به الخاتمة. تخطي إذا كان هذا الحقل 0. |
| 0x32 | 1 | قسم غير محلول | الفهرس في جدول القسم الذي لم يتم حله متعلق بـ. تخطي إذا كان هذا الحقل 0. |
| 0x33 | 1 | قسم bss | فهرس في جدول القسم الذي يرتبط bss به. ممتلئة في وقت التشغيل! |
| 0x34 | 4 | برولوج | الإزاحة في قسم محدد من وظيفة _prolog. |
| 0x38 | 4 | الخاتمه | إزاحة في قسم محدد من وظيفة _epilog. |
| 0x3c | 4 | دون حل | الإزاحة في قسم محدد من الدالة _unresolved. |
| 0x40 | 4 | محاذاة | الإصدار ≥ 2 فقط. قيد المحاذاة على كافة الأقسام ، معبرًا عنه بقوة 2. |
| 0x44 | 4 | bssAlign | الإصدار ≥ 2 فقط. قيد المحاذاة في جميع أقسام '.bss' ، معبرًا عنه بقوة 2. |
| 0x48 | 4 | الإصلاحالحجم | الإصدار ≥ 3 فقط. إذا تم ربط REL بـ OSLinkFixed (بدلاً من OSLink) ، يمكن استخدام المساحة بعد هذا العنوان لأغراض أخرى (مثل BSS). |

### جدول معلومات القسم
يحتوي جدول معلومات القسم على ** عدد أقسام ** إدخالات كل 0x8 بايت بطول:
| الأوفست | الحجم | الوصف |
-------|------------|-------------|
| 0x0 | 30 بت | الإزاحة من بداية REL إلى القسم. إذا كان هذا هو الصفر ، فإن القسم هو قسم غير مهيأ (على سبيل المثال .bss). |
| 0x3.6 | 1 بت | مجهول. |
| 0x3.7 | 1 بت | علم قابل للتنفيذ إذا كان هذا هو 1 القسم قابل للتنفيذ. |
| 0x4 | 4 | الطول بالبايت من المقطع. إذا كان هذا صفرًا ، فسيتم تخطي هذا الإدخال. |
| 0x8 | الإدخال التالي | الإدخال التالي |

### بيانات النقل
بيانات إعادة التوطين هي قائمة واحدة أو أكثر من هياكل البايت 0x8. يتم تمييز نهاية كل قائمة برمز النوع الخاص 203:
| الأوفست | الاسم | الحجم | الوصف |
-------|------------|------------|-----|
| 0x0 | تعويض | 2 | الإزاحة بالبايت من النقل السابق إلى هذا. إذا كان هذا هو الانتقال الأول في القسم ، فهذا يتعلق ببداية القسم. |
| 0x2 | اكتب | 1 | نوع النقل. هو موضح أدناه. |
| 0x3 | قسم | 1 | قسم الرمز المراد الانتقال إليه. بالنسبة لنوع النقل الخاص 202 ، يكون هذا بدلاً من ذلك رقم القسم في هذا الملف الذي تنطبق عليه إدخالات إعادة التوطين التالية. |
| 0x4 | إضافة | 4 | الإزاحة بالبايت للرمز المراد الانتقال إليه ، بالنسبة إلى بداية قسمه. هذا هو العنوان المطلق بدلاً من ذلك لعمليات الترحيل مقابل main.dol. |
| 0x8 | الإدخال التالي | الإدخال التالي | الإدخال التالي |


 




## مراجع


* [تنسيق وحدة الكائن القابل للنقل] (https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)

