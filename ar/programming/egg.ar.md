{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف EGG - ملف توزيع بايثون" ,
  "description":"تعرف على تنسيق ملف EGG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات EGG وفتحها." ,
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-03-15"
}

## ما هو ملف EGG؟

ملف EGG ، المعروف أيضًا باسم بيض Python ، هو تنسيق توزيع أقدم من توزيعات Python. إنه [ZIP](/ar/ compression / zip /) أرشيف مضغوط بامتداد .egg ويحتوي على ملفات مصدر تطبيق Python جنبًا إلى جنب مع معلومات التعريف حول التوزيع. تعد ملفات EGG بديلاً لملف Windows Executable [EXE](/ar/ قابل للتنفيذ / exe /) ولكنها تعمل عبر الأنظمة الأساسية. تم استبدال هذا التنسيق القديم لتوزيعات Python بتنسيق ملف Wheel (WHL) الأحدث في أوائل عام 2010.

## تنسيق ملف EGG

يتم حفظ ملفات EGG كملفات أرشيف مضغوطة. هذا يعني أنك إذا استبدلت الامتداد .egg بـ .zip ، فستتمكن من فتحه باستخدام أدوات إزالة الضغط القياسية مثل Corel WinZIP أو Microsoft Explorer أو RARLAB WinRAR.

يمكن إنشاء ملفات EGG باستخدام حزمة ** distutils ** المتاحة بواسطة Python. هناك أداة أخرى يمكنها إنشاء ملفات EGG وفتحها وهي ** SetupTools **. يمكن تثبيت ملفات EGG كحزمة باستخدام ** easy_install **.

`ملاحظة - تم تجاوز تنسيق ملف EGG لصالح تنسيق ملف WHL الجديد

## المرجعي ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)

