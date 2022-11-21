{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف HDR - ما هو ملف صورة HDR؟",
  "description":"تعرف على تنسيق ملف HDR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات HDR وفتحها." ,
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2022-07-21"
}

## ما هو ملف HDR؟

ملف HDR هو تنسيق ملف صورة نقطية ذات نطاق ديناميكي عالٍ (HDR) لتخزين صور الكاميرا الرقمية. يسمح لمحرري الصور بتحسين لون وسطوع الصور الرقمية ذات النطاق الديناميكي المحدود. يمكن أن يؤدي هذا التعديل إلى تحسين السطوع حول الزوايا ، مما ينتج عنه صورة قريبة من الطبيعة. عادةً ما يتم حفظ ملفات HDR كصور نقطية 32 بت. يمكن لبرنامج Adobe Photoshop إنشاء ملفات HDR وفتحها.

تُعرف ملفات HDR أيضًا باسم HDRI.

## تنسيق ملف HDR - مزيد من المعلومات

يعتمد تنسيق ملف HDR على تنسيق ملف Radiance Picture (.pic) الأصلي. عادةً ما يتم تخزين بيانات البكسل الخاصة بملف HDR غير مضغوطة ، ولكن في بعض الحالات يتم ضغطها باستخدام نظام تشفير بطول التشغيل المباشر.

### هيكل ملف HDR

يتكون ملف صورة HDR من الأقسام الثلاثة التالية:

* ** Header: ** يتم تحديد ملف HDR بواسطة البايتات الأولى في ملف الصورة مثل "#؟ RADIANCE".
* ** سلسلة الدقة: ** يتبع العنوان سطر دقة واحد يتكون من 4 قيم ؛ علامة X و Y متبوعة بقيمة عددية عددية. يشير ترتيب X و Y إلى الدوران. إن الجمع بين X و Y مع القيم الموجبة والسالبة يغطي جميع الاتجاهات والدورات الممكنة.
* ** بيانات البكسل: ** بيانات البكسل لملف HDR إما غير مضغوطة أو مضغوطة باستخدام ترميز طول التشغيل القياسي.

## واجهات برمجة تطبيقات HDR / HDRI مفتوحة المصدر

* ** [imageinfo] (https://github.com/xiaozhuai/imageinfo) ** - مكتبة برأس واحد فائقة السرعة عبر النظام الأساسي [C ++] (/ar/ برمجة / cpp /) للحصول على حجم الصورة وتنسيقها دون تحميل / فك تشفير.
* ** [imgaeinfo-rs] (https://github.com/xiaozhuai/imageinfo-rs) ** - مكتبة الصدأ للحصول على حجم الصورة وتنسيقها دون تحميل / فك تشفير. يدعم [.avif] (/ar/ image / avif /) ، [.bmp] (/ar/ image / bmp) ، [.cur] (/ar/ image / cur /) ، [.dds] (/ar/ image / dds /) ، [. gif] (/ar/ image / gif /) ، hdr (pic) ، [heic (heif)] (/ar/ image / heic /) ، [.icns] (/ar/ image / icns /) ، [.ico] (/ar/ image / ico /) ، [.jp2] (/ar/ image / jp2 /) ، [jpeg (jpg)] (/ar/ image / jpeg /) ، [jpx] (/ar/ image / jpx /) ، ktx ، [png] (/ar/ image / png /) و [psd] (/ar/ image / psd /) و qoi و tga و tiff (tif) و webp.
* ** [HdrHistogram] (https://github.com/HdrHistogram/HdrHistogram) ** - تنفيذ Java لـ HdrHistogram.

## مراجع

* [Radiance HDR] (http://paulbourke.net/dataformats/pic/)
* [imageinfo] (https://github.com/xiaozhuai/imageinfo)

