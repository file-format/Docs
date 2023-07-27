{
  "date" : "2020-01-12",
  "keywords" :["DGN", "File", "Format", "Open", "Read", "API", "MicroStation", "Intergraph Interactive Graphics Design System"],
  "author" :{
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - تنسيق ملف تصميم MicroStation CAD" ,
  "description" :"تعرف على تنسيق ملف DGN وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DGN وفتحها." ,
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
} ,
  "lastmod" : "2020-01-12"
}

## ما هو ملف DGN؟

الملف ذو الامتداد .dgn (التصميم) هو ملف رسم تم إنشاؤه بواسطة تطبيقات CAD ودعمها مثل MicroStation و Intergraph Interactive Graphics Design System. يتم استخدامه لإنشاء وحفظ التصاميم لمشاريع البناء مثل الطرق السريعة والجسور والمباني. يشبه التنسيق تنسيق ملف Autodesk [DWG](/ar/cad/dwg/) ويعتبر منافسًا له. يمكن حفظ ملفات DNG بتنسيق ملف Intergraph القياسي أو V8 DGN. يمكن تحويل DGN إلى عدة تنسيقات أخرى مثل DWG ، [BMP](/ar/image/bmp/) ، [JPEG](/ar/image/jpeg/) ، [PDF](/ar/pdf/) ، [GIF](/ar/image/gif/) وغيرها. يمكن فتحه باستخدام Autodesk AutoCAD و Bentley View و Bentley Systems MicroStation بالإضافة إلى تطبيقات برمجية أخرى مثل إصدارات Corel PaintShop Photo Pro و IMSI TurboCAD Deluxe.

## تنسيق ملف V8 DGN

يتكون ملف MicroStation V8 DGN من نموذج واحد أو أكثر. النموذج هو وعاء للعناصر. يزيل V8 DGN جميع القيود المستندة إلى تنسيق الملفات التي كانت موجودة في الإصدارات السابقة من MicroStation. فيما يلي قائمة بالتحسينات في تنسيق ملف DGN.

* تمت إزالة الحد على عدد المستويات في ملف DGN ، وتم تسمية كل مستوى وتخزينه كعنصر.
* الحجم الفعلي الأقصى لملف DGN ليس له أي قيود وهو مقيد فقط من قبل نظام التشغيل (مثل حد NT هو 4 جيجابايت)
* الحد الأقصى لحجم العنصر الواحد هو 128 كيلوبايت.
* لا يوجد حد أقصى لحجم الخلية.
* تقتصر أسماء الخلايا على 500 حرف تقريبًا.
* لا يوجد حد لعدد المراجع التي يمكن إرفاقها بملف DGN.
* يمكن أن يصل طول الخط أو الشكل أو منحنى النقطة إلى 5000 رأس.
* لا يوجد حد لعدد المكونات في سلسلة معقدة أو شكل معقد.
* لا يوجد حد لعدد مجموعات الرسوم في ملف DGN.
* السور موازٍ للمنظر الذي وُضع فيه.
* يمكن أن يحتوي سطر النص الواحد على 65.535 حرفًا.
* لا يوجد حد أقصى لحجم العقدة النصية.
* لا يوجد حد لعدد العقد النصية في ملف DGN.
* يحتوي كل عنصر على معرف 64 بت فريد لا يتغير خلال دورة حياة العنصر.
* يحتوي كل عنصر على طابع زمني يشير إلى وقت التغيير الأخير.

## مراجع

* [DNG - بواسطة Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [تنسيق ملف MicroStation V8 DGN](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

