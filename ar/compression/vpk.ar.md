{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف VPK - تنسيق ملف حزمة تطبيق PlayStation Vita" ,
  "description":"تعرف على تنسيق ملف VPK وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VPK وفتحها." ,
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2022-03-01"
}

## ما هو ملف VPK؟

الملف بامتداد .vpk هو ملف حزمة أرشيف مضغوط يستخدم لتثبيت تطبيقات الطرف الثالث على وحدة تحكم ألعاب Sony PlayStation Vita. يمكن تثبيت هذه الملفات فقط على jailbreak Vita PlayStation by HENkaku الذي مكّن PS Vita و PSTV من استخدام محتوى مخصص تم إنشاؤه بواسطة المستخدم. يحتوي ملف أرشيف VPK على جميع المحتويات التي تتكون منها اللعبة بما في ذلك الصور مثل ملفات [PNG](/ar/ image / png /) وإعداد الملفات مثل [.bin](/ar/ disc-and-media / bin /) ، و أي تكوينات في تنسيق ملف [XML](/ar/ web / xml /).

## تنسيق ملف VPK

يتم حفظ ملفات VPK على القرص كأرشيف مضغوط قياسي [ZIP](/ar/ compression / zip /). قد تحتوي على مجلدات متعددة وملفات أخرى مرتبطة لتطبيقات الطرف الثالث ليتم تثبيتها على Vita Gaming Console. لعرض محتويات ملف حزمة VPK ، أعد تسمية امتداده من .vpu إلى .zip ، واستخرج المحتويات باستخدام أدوات إزالة الضغط القياسية مثل WinZip أو WinRAR.

يحتوي برنامج Valvesoftware على معلومات مفصلة حول [تنسيق ملف VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) التي يمكن الرجوع إليها من منظور المطور.

## كيفية تثبيت ملفات VPK؟

يمكن تثبيت ملفات VPK من الأداة المساعدة لسطر الأوامر VPK.exe. في نظام التشغيل Windows OS ، يمكن إسقاط الملفات على ملف vpk.exe الذي يقوم بإرجاع الملف \ *. vpk الذي يحتوي على كافة الملفات التي تم حزمها. بدلاً من ذلك ، يمكن استخدام أداة سطر الأوامر على النحو التالي.

### إنشاء VPK وإضافة ملفات

```
vpk <dirname>
```

### استخراج ملفات VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## عارض VPK

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## مراجع

* [تنسيق ملف VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [ملفات VPK](https://developer.valvesoftware.com/wiki/VPK)

