{
  "date" : "2020-08-20",
  "keywords" :["ملف eot" , "تنسيق ملف eot" , "ما هو ملف eot" , "ملف" , "eot example" , "امتداد ملف eot" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - تنسيق ملف خط TrueType" ,
  "description":"تعرف على تنسيق ملف EOT وواجهات برمجة التطبيقات لإنشاء ملفات EOT وفتحها." ,
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
} ,
  "lastmod" : "2020-10-21"
}

## ما هو ملف EOT؟

الملف ذو الامتداد .eot هو خط OpenType مضمن في المستند. تستخدم هذه في الغالب في ملفات الويب مثل صفحة الويب. تم إنشاؤه بواسطة Microsoft وهو مدعوم من قبل منتجات Microsoft بما في ذلك ملف PowerPoint التقديمي [.pps](/ar/presentation/pps/). الملف ليس للاستخدام الأساسي وهو نوع من المستند المصاحب للمستند الرئيسي أو صفحة الويب. على غرار خطوط OTF ، تدعم EOT كلاً من مخططات Postscript و TrueType للحروف الرسومية. تكون ملفات EOT أصغر حجمًا بسبب ضغطها باستخدام ضغط LZ. يستخدم EOT أداة Microsoft لإنشاء خط من خطوط TTF / OTF الموجودة.

## نبذة تاريخية

تم تقديم خط EOT إلى W3C في عام 2007 كجزء من CSS3 ولكن نظرًا لمتطلباته ليتم تثبيته بشكل دائم على نظام بعيد أصبح سبب رفضه. تمت إعادة تقديمه في مارس 2008 ، لكن W3C اختار في النهاية [تنسيق خط الويب](/ar/font/woff/) (WOFF) والذي تم توحيده في ذلك الوقت.

## تنسيق ملف EOT

يمكن العثور على تفاصيل تنسيق ملف EOT على [صفحة إرسال W3](https://www.w3.org/Submission/EOT/#FileFormat) وتوضح البنية المستخدمة بواسطة تنسيق الخط هذا. يتكون EOT من بنية EMBEDDEDFONT واحدة توفر معلومات أساسية كافية حول اسم خط hte والأحرف المدعومة. تتيح تعبئة هذه المعلومات لوكلاء المستخدم تجنب تفريغ الخط أو فك ضغطه أو تثبيته إذا كان موجودًا بالفعل على الجهاز.

### هيكل EMBEDDEDFONT
خضع هيكل EMBEDDEDFONT لثلاثة مراجعات ، مع إضافة بيانات إضافية في نهاية الهيكل مع كل مراجعة. المراجعة الأخيرة لهيكل EMBEDDEDFONT كما هو موضح أدناه.

| نوع البيانات | اسم الإدخال | الوصف |
---|---|---|
| طويل بدون إشارة | حجم EOTSize | إجمالي طول البنية بالبايت (بما في ذلك بيانات السلسلة والخط) |
| طويل بدون توقيع | FontDataSize | طول خط OpenType (FontData) بالبايت |
| طويل بدون توقيع | الإصدار | رقم إصدار هذا التنسيق - 0x00020002 |
| بدون إشارة طويلة | أعلام | أعلام معالجة |
| بايت [10] | FontPANOSE | قيمة PANOSE لهذا الخط - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan |
| بايت | Charset | في Windows ، هذا مشتق من TEXTMETRIC.tmCharSet. تحدد هذه القيمة مجموعة أحرف الخط. يشير DEFAULT_CHARSET (0x01) إلى عدم وجود تفضيل. - راجع https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica |
| بايت | مائل | إذا تم تعيين بت ITALIC في OS / 2.fsSelection ، ستكون القيمة 0x01 - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss |
| الطول | الوزن | قيمة الوزن لهذا الخط - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc |
| قصير | fsType | إشارات النوع التي توفر معلومات حول أذونات التضمين - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst |
| اختصار | MagicNumber | الرقم السحري لملف EOT - 0x504C. يُستخدم للتحقق من وجود تلف في البيانات
| طويل بدون توقيع | UnicodeRange1 | نظام التشغيل / 2.UnicodeRange1 (بت 0-31) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur |
| طويل بدون توقيع | UnicodeRange2 | نظام التشغيل / 2.UnicodeRange2 (بت 32-63) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur |
| طويل بدون توقيع | UnicodeRange3 | نظام التشغيل / 2.UnicodeRange3 (بت 64-95) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur |
| طويل بدون توقيع | UnicodeRange4 | نظام التشغيل / 2.UnicodeRange4 (بت 96-127) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur |
| طويل بدون توقيع | CodePageRange1 | CodePageRange1 (بت 0-31) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr |
| طويل بدون توقيع | CodePageRange2 | CodePageRange2 (بت 32-63) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr |
| بدون توقيع طويل | تعديل المجموع الاختباري | head.CheckSumAdjustment - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/head |
| بدون توقيع طويل | محجوز 1 | محجوز - يجب أن يكون 0 |
| بدون توقيع طويل | محجوز 2 | محجوز - يجب أن يكون 0 |
| بدون توقيع طويل | محجوز 3 | محجوز - يجب أن يكون 0 |
| بدون توقيع طويل | محجوز 4 | محجوز - يجب أن يكون 0 |
| قصير بدون إشارة | Padding1 | حشوة للحفاظ على المحاذاة الطويلة. يجب دائمًا تعيين قيمة المساحة المتروكة على 0x0000. |
| قصير بدون توقيع | FamilyNameSize | عدد البايت المستخدم بواسطة صفيف FamilyName |
| بايت | FamilyName [FamilyNameSize] | صفيف من أحرف UTF-16 بطول FamilyNameSize بايت. هذه هي سلسلة مجموعة خطوط اللغة الإنجليزية الموجودة في جدول الاسم الخاص بالخط (اسم المعرف = 1) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/name |
| يجب تعيين قيمة | Padding2 | القصير غير الموقعة على قيمة المساحة المتروكة إلى 0x0000. |
| قصير بدون توقيع | StyleNameSize | عدد البايت المستخدم بواسطة StyleName |
| بايت | StyleName [StyleNameSize] | صفيف من أحرف UTF-16 بطول StyleNameSize بايت. هذه هي سلسلة الفئة الفرعية للخط باللغة الإنجليزية والموجودة في جدول أسماء الخط (اسم المعرف = 2) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/name |
| يجب تعيين قيمة | Padding3 | القصير غير الموقعة على قيمة المساحة المتروكة إلى 0x0000. |
| قصير بدون توقيع | VersionNameSize | عدد البايت المستخدمة من قبل VersionName |
| بايت | VersionName [VersionNameSize] | صفيف من أحرف UTF-16 بطول VersionNameSize بايت. هذه هي سلسلة إصدار اللغة الإنجليزية الموجودة في جدول الاسم الخاص بالخط (اسم المعرف = 5) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/name |
| يجب تعيين قيمة | Padding4 | القصير غير الموقعة على قيمة المساحة المتروكة إلى 0x0000. |
| قصير بدون توقيع | FullNameSize | عدد البايت المستخدمة من قبل FullName |
| بايت | FullName [FullNameSize] | صفيف من أحرف UTF-16 بطول FullNameSize بايت. هذه هي سلسلة الاسم الكامل باللغة الإنجليزية الموجودة في جدول الاسم الخاص بالخط (اسم المعرف = 4) - راجع https://learn.microsoft.com/en-us/typography/opentype/spec/name |
| يجب تعيين قيمة | Padding5 | القصير غير الموقعة على قيمة المساحة المتروكة إلى 0x0000. |
| قصير | RootStringSize | عدد البايت المستخدم بواسطة صفيف RootString |
| بايت | RootString [RootStringSize] | صفيف من أحرف UTF-16 بطول بايت RootStringSize.
| طويل بدون توقيع | RootStringCheckSum | قيمة المجموع الاختباري لـ RootString. راجع الخوارزمية لمعالجة RootStringChecksum أدناه. |
| طويل بدون توقيع | EUDCCodePage | قيمة صفحة الترميز المطلوبة لدعم خط EUDC. |
| يجب تعيين قيمة | Padding6 | القصير غير الموقعة على قيمة المساحة المتروكة إلى 0x0000. |
| قصير بدون توقيع | SignatureSize | عدد البايت المستخدم بواسطة صفيف التوقيع. محجوز حالياً ويجب تعيينه إلى 0x0000. |
| بايت | التوقيع [SignatureSize] | محجوز حاليًا. إذا كان SignatureSize هو 0x0000 فلا يوجد طول لهذا الصفيف. |
| طويل بدون توقيع | EUDCFlags | معالجة الإشارات لخط EUDC. قد تكون القيم النموذجية TTEMBED_XORENCRYPTDATA و TTEMBED_TTCOMPRESSED.
| طويل بدون توقيع | EUDCFontSize | عدد البايت المستخدم من قبل صفيف التوقيع. |
| بايت | EUDCFontData [EUDCFontSize] | عدد البايت المستخدم لبيانات خط EUDC. إذا كان حجم EUDCFontSize هو 0x00000000 فلا يوجد طول لهذا الصفيف. |
| بايت | FontData [FontDataSize] | بيانات الخط لملف EOT هذا. قد تكون البيانات مضغوطة أو مشفرة XOR كما هو مشار إليه بواسطة إشارات المعالجة

## مراجع

* [تنسيق ملف EOT](https://www.w3.org/Submission/EOT/)
* [OpenType مضمن](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [تضمين الخط](https://en.wikipedia.org/wiki/Font_embedding)

