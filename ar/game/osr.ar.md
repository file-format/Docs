{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"ملف OSR - osu! إعادة تشغيل تنسيق الملف",
  "title" : "ملف OSR - osu! إعادة تشغيل تنسيق الملف",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ما هو ملف OSR؟

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

** نوع MIME لتنسيق ملف OSR: ** x-osu-replay

## تنسيق ملف أوسر

يتم حفظ ملفات OSR كملفات ثنائية ذات حقول بيانات ثابتة ومتغيرة الطول.

|نوع البيانات| تنسيق|
---|---|
|Byte |وضع اللعبة في الإعادة (0 = osu! Standard، 1 = Taiko، 2 = Catch the Beat، 3 = osu!mania)|
|عدد صحيح |إصدار اللعبة عندما تم إنشاء الإعادة (مثال: 20131216)|
|سلسلة |أوسو! خريطة الضرب MD5 التجزئة |
|سلسلة| اسم اللاعب|
|سلسلة| أوسو! إعادة تشغيل تجزئة MD5 (تتضمن خصائص معينة للإعادة)|
|قصير| عدد 300 ثانية|
|قصير| عدد 100 في المعيار، 150 في تايكو، 100 في CTB، 100 في الهوس |
|قصير| عدد 50 في الفاكهة القياسية، صغيرة في CTB، 50 في الهوس|
|قصير| عدد Gekis في المستوى القياسي، بحد أقصى 300 ثانية في الهوس|
|قصير| عدد الكاتوس في المعيار، 200 في الهوس|
|قصير| عدد الأخطاء|
|عدد صحيح| مجموع الدرجات المعروضة في تقرير الدرجات|
|قصير| أعظم التحرير والسرد المعروضة في تقرير النتيجة|
|بايت| التحرير والسرد المثالي/الكامل (1 = لا توجد أخطاء ولا فواصل شريط التمرير ولا توجد أشرطة تمرير منتهية مبكرًا)|
|عدد صحيح| تعديل المستخدمة. انظر أدناه للحصول على قائمة بقيم التعديل.|
|سلسلة| الرسم البياني لشريط الحياة: أزواج مفصولة بفواصل u/v، حيث u هو الوقت بالمللي ثانية في الأغنية وv هي قيمة النقطة العائمة من 0 إلى 1 التي تمثل مقدار الحياة لديك في الوقت المحدد (0 = شريط الحياة هو فارغ، 1= شريط الحياة ممتلئ)|
|طويل| الطابع الزمني (علامات التجزئة في Windows)|
|عدد صحيح| الطول بالبايت من بيانات إعادة التشغيل المضغوطة|
|بايت |صفيف بيانات إعادة التشغيل المضغوطة|
|طويل| معرف النتيجة على الانترنت|
|مزدوج| معلومات تعديل إضافية. موجود فقط إذا تم تمكين التدريب على الهدف.|

## مراجع

* [جامعة ولاية أوهايو! لعبة الإيقاع](https://osu.ppy.sh/home)
* [تنسيق ملف OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)