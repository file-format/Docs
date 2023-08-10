{
  "date" : "2021-10-20",
  "keywords" :[".pak" , "تنسيق الملف" , "ما هو ملف pak" , "ملف" , "مثال pak" , "ملف حزمة لعبة فيديو" , "امتداد"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على ملف .pak وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PAK وفتحها." ,
  "title" :"تنسيق ملف PAK- ملف حزمة ألعاب الفيديو" ,
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
} ,
  "lastmod" : "2021-10-27"
}

## ما هو ملف PAK؟

ملف PAK هو ملف حزمة تم إنشاؤه بواسطة ألعاب فيديو مختلفة لأرشفة بيانات اللعبة. في الأساس ، إنه تنسيق ملف لعبة. يمكن أن يتضمن ذلك عناصر متعددة للعبة مثل الرسومات والقوام والأصوات والأشياء بالإضافة إلى بيانات اللعبة الأخرى. يتم حفظ الأرشيف في الغالب كملف .zip ويمكن استخراجه باستخدام برامج فك الضغط الشائعة مثل WinZip و WinRAR. تتضمن أمثلة ألعاب الفيديو التي تستخدم ملفات PAK Quake و Hexen و Crysis و Half-Life.

## تنسيق ملف PAK - مزيد من المعلومات

في معظم الحالات ، يتم حفظ ملفات PAK في [تنسيق ملف ZIP](/ar/compression/zip/). لكن التطبيقات المختلفة قد تستخدم تنسيق ملف مختلفًا لتخزين هذه الملفات.


## كيف تفتح ملفات PAK؟

يمكنك فتح ملفات PAK بتطبيقات مثل [PakExplorer](https://www.quaketerminus.com/tools.shtml) و [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

** ------------------------------------------------ -------------------------------------------------- ----------------------- **

## تنسيق ملف PAK - ملف كائن Simutrans

الملف ذو الامتداد .pak هو تنسيق ملف لعبة محاكاة النقل [Simutrans](https://www.simutrans.com/en/). يحتوي على كائنات مستخدمة في المحاكاة مثل الرسومات التي صنعها المستخدم ومحتويات البيانات. يمكن أن تحتوي على العديد من الكائنات المختلفة مثل مركبات الألعاب والمباني والتضاريس وما إلى ذلك. يتم إنشاء ملفات PAK باستخدام MakeObject ، وهي أداة تقوم بتجميع ملفات .dat وصور .png لإنشاء كائنات المحاكاة هذه. يتيح Simutrans للاعبين تشغيل نظام نقل ناجح من خلال إنشاء وإدارة أنظمة النقل للركاب والبريد والبضائع عن طريق البر

## كيفية إنشاء ملفات PAK؟

قام Simutrans بسرد أمثلة نموذجية لإنشاء ملفات PAK على نظامي التشغيل Windows و Linux.

### نظام تشغيل Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### نظام Linux BE / OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## مراجع

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)