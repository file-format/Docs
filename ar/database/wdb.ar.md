{
  "date" : "2021-08-24",
  "keywords" :["wdb file", "wdb file format", "what is a wdb file", "file", "wdb example", "wdb file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف WDB وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات WDB وفتحها." ,
  "title" :"WDB - ملف تتبع SQL Server" ,
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2021-08-24"
}

## WDB ما ه
الملف بامتداد .wdb هو في الواقع ملف قاعدة بيانات تم إنشاؤه بواسطة Microsoft Works والذي تم استخدامه لأداء وظائف مثل نظام إدارة قاعدة البيانات. ملف WDB مشابه لملف Access Database ([MDB] (/ar/ database / mdb /)) ، لكنه أقل كفاءة وقيود أكبر. لا يمكن فتح ملفات WDB باستخدام Microsoft Access. ومع ذلك ، يمكنك فتح ملف WDB في Microsoft Works ثم تصديره إلى ملف MDB ، من أجل فتح ملف WDB في MS Access.

## تنسيق ملف WDB
قاعدة بيانات Microsoft Works هي تنسيق قاعدة البيانات الأصلي لمجموعة Microsoft Works Office. بسبب طبيعة الملكية للشكل وبعض القيود. لا يمكن فتح ملفات WDB في أي برنامج آخر غير Microsoft Works. في تنسيق الملف ، يمكن العثور على رأس متكرر 10 بايت قبل كل سلسلة نصية ASCII تمثل قيم الحقول التي تم إنهاؤها بقيمة NULL. يبدأ الرأس عمومًا بـ ** \ x0f ** بايت و NULL ، متبوعًا بـ 4 بايت بيانات بالتناوب مع القيم الخالية.

### بنية الملف

فيما يلي هيكل ملف WDB:
- ** العنوان الأول **: من بداية الملف وتنتهي بـ \ x25 \ x00 \ xf2 و 244 بايت NULL
- ** العنوان الثاني **: يبدأ بـ \ xffT - أي \ xff \ x54 ويمتد لـ 4096 بايت ، والذي يحتوي على أسماء الأعمدة / الحقول وأشياء أخرى ، ويبدو أنه يبدأ عند موضع البايت 6144.
- ** الحقل **: القيمة لها رأس 10 بايت ، بالتنسيق التالي: {type byte} {type byte، part 2} {data byte 1} \ x00 {db 2} \ x00 {db 3} {db 3 ، الجزء 2} {ديسيبل 4} \ x00. بايت البيانات 2 هو رقم الحقل ، بايت البيانات 3 هو رقم السجل (إضافة بايت 3 ، الجزء 2 عندما يتجاوز 256 سجلًا).


## مراجع ##

* [المستخدم: تنسيق JesseW / wdb] (https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

