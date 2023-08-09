{
  "date" : "2021-09-08",
  "keywords" :["ملف mgx" , "تنسيق ملف mgx" , "ما هو ملف mgx" , "ملف" , "مثال mgx" , "امتداد الملف mgx" , "extension" , "format"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف Age of Empires 2 Expansion Replay وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MGX وفتحها." ,
  "title" :"MGX - Age of Empires 2 Expansion Replay" ,
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
} ,
  "lastmod" : "2021-09-08"
}

## MGX ما ه

الملف بامتداد .mgx هو ملف مسجل لـ Age of Empires II: The Conquerors يمكن إعادة تشغيله ضمن برنامج Age of Empires II. يحتوي على تسجيل كامل للحملة التي قام بها المستخدم. يمكن تحميلها وتشغيلها في برنامج Age of Empires II. بمجرد إعادة التشغيل ، تعرض اللعبة جميع الأحداث والسيناريوهات التي خطط المستخدم للحملة ولعبها.

## تنسيق ملف MGX - مزيد من المعلومات

تم إعداد تنسيق الملف الداخلي لملف MGX وإتاحته كمعلومات تم التحقق من صحتها جزئيًا حول [Age of Empires 2: The Conquerors - Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). تحدد المواصفات التفاصيل في الأقسام التالية.

### تعريفات الهيكل

يُعتقد أن تعريفات بنية تنسيق ملف GPX تستند إلى [تصريحات BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) التي توفر طريقة لقراءة البيانات الثنائية المنظمة وكتابتها. يتيح هذا للمبرمج تحديد تنسيق البيانات الثنائية التي يتم قراءتها وكتابتها بواسطة BinData.

### المراسلة MGX

تعتمد رسائل MGX على نوعين من الرسائل.

* GAMESTART - تحدد أوامر بدء اللعبة ولم يتم التحقق من صحتها حتى الآن
* الدردشة - تصف رسائل الدردشة داخل اللعبة. يمكن للاعبين واللعبة نفسها (Gaia) إرسال رسائل داخل اللعبة.

### إجراءات اللعب

هناك العديد من [إجراءات GAMEPLAY](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) التي تم استردادها وتفاصيلها متاحة.

## مراجع

* [Age of Empires 2: The Conquerors - Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)

