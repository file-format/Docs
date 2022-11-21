{
  "date" : "2022-04-01",
  "keywords" :["nkit file", "nkit file format", "what is a nkit file", "file", "nkit example", "nkit file extension", "extension", "format", "nkit footer", "file تنسيق nkit "] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
   "toc" : true,
  "description" :"تعرف على تنسيق ملف NKIT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات NKIT وفتحها." ,
  "title" :"NKIT - تنسيق ملف صورة القرص" ,
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
} ,
  "lastmod" : "2022-04-01"
}

## ما هو ملف NKIT؟

ملف NKIT هو صورة قرص للبيانات المستخرجة من ألعاب NintendoWii و GameCube. NKIT مخصص لتنسيق مجموعة أدوات Nintendo. يستخدم ملف الضغط الناتج [ISO] (/ar/ compression / iso /) البيانات الرئيسية لهذه الألعاب ليتم تشغيلها مع برامج المحاكاة مثل Dolphin و Swiss و Nintendont. يأتي NKit بتنسيقات ملفات خام (iso) adn مضغوطة (gcz) والتي تم تصميمها مع مراعاة إمكانية تشغيل العرض وحجمه.

## تنسيق ملف NKIT

تنسيق ملف NKit هو تنسيق غير ضياع ويستخدم لتقليص واستعادة صور Nintendo Wii و GameCube. تتوفر التنسيقات بتنسيقات ملفات ISO و GCZ لكل من ألعاب GameCube و Wii.

| النظام | التنسيق | الأجهزة المدعومة | Dolphin المدعوم | قابل للترميم 1: 1 | ملاحظات |
---|---|---|---|---|---|
| جيم كيوب | nkit.iso | نعم | نعم | نعم | نفس GameCube iso المضغوط |
| جيم كيوب | nkit.gcz | لا | نعم | نعم | GCZ هو تنسيق ضغط بلوك خاص بـ Dolphin يمكن البحث عنه |
| وي | nkit.iso | لا نعم | نعم | يمكن تشغيل تنسيق RVT-H فقط في Dolphin |
| وي | nkit.gcz | لا نعم | نعم | RVT-H في GCZ قابل للعب في Dolphin فقط |

### رأس NKIT

يكون عنوان تنسيق ملف NKIT كما يلي.

| الإزاحة | الطول | الاسم |
---|---|---|
| 0x200 | 0x4 | رأس NKit 'NKIT' |
| 0x204 | 0x4 | إصدار NKit 'v01' |
| 0x208 | 0x4 | مصدر الصورة الأصلي CRC32 |
| 0x20C | 0x4 | NKit CRC - يجعل ملف NKit CRC32 مساويًا لمصدر CRC عند 0x208 (عند 0x4 في GCZ) |
| 0x210 | 0x4 | طول صورة المصدر |
| 0x214 | 0x4 | معرف غير هام إجباري (عند اختلاف معرف القرص - نادر - GameCube فقط) |
| 0x218 | 0x4 | قسم تحديث Wii CRC32 إذا تمت إزالته عند التحويل |

## مراجع ##

* [تنسيق ملف NKIT - بواسطة gbatemp] (https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

