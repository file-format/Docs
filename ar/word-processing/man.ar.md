{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix Manual" ,
  "description":"تعرف على تنسيق ملف FODT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MAN وفتحها." ,
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
} ,
  "lastmod" : "2021-07-25"
}

## ما هو ملف MAN؟

يشير الملف بامتداد .man إلى صفحة man وهي دليل مستخدم لبرمجة Unix في نموذج توثيق البرنامج. يتم استخدامه بواسطة الأداة المساعدة "Man" المضمنة في Unix ، والتي تُستخدم لعرض الوثائق. تحتوي وثائق البرنامج على معلومات في أقسام وصفحات يمكن استردادها باستخدام الأداة المساعدة Man من محطة الأوامر عن طريق إصدار الأوامر. كونها متاحة على الكمبيوتر كنسخة إلكترونية من الوثائق ، فإنها لا تتطلب أي نسخة مطبوعة أو اتصال بالإنترنت للوصول إليها.

## تنسيق ملف Unix Manual Man - مزيد من المعلومات

يتم تخزين صفحات الإنسان بتنسيق نص عادي ويمكن إنشاؤها وفتحها في أي محرر نصوص للعرض أو التحرير. في UNIX ، يتم استرداد المعلومات من صفحات Man عن طريق إصدار أوامر من المحطة التي تتضمن مرجعًا لأرقام الأقسام والصفحات من الدليل.

### الأقسام والصفحات

Unix man هو دليل النظام حيث تشير كل صفحة إلى الأمر إلى اسم البرنامج أو الأداة المساعدة أو الوظيفة. سيبحث الأمر ، إذا تم تزويده بمعلومات القسم ، عن الصفحة في هذا القسم المحدد. ومع ذلك ، فإن السلوك الافتراضي هو البحث عن الصفحة في جميع الأقسام وعرض الصفحة الأولى بغض النظر عما إذا كانت موجودة في أقسام متعددة.

### أرقام الأقسام

فيما يلي معلومات حول أرقام أقسام الدليل متبوعة بأنواع الصفحات التي يحتوي عليها.

| رقم المقطع | نوع الصفحات |
---|---|
| 1 | البرامج القابلة للتنفيذ أو أوامر shell |
| 2 | استدعاءات النظام (الوظائف التي يوفرها kernel) |
| 3 | استدعاءات المكتبة (وظائف ضمن مكتبات البرامج) |
| 4 | ملفات خاصة (توجد عادة في / dev) |
| 5 | تنسيقات واصطلاحات الملفات ، على سبيل المثال / etc / passwd |
| 6 | ألعاب |
| 7 | متفرقات (بما في ذلك حزم ماكرو واصطلاحات) ، على سبيل المثال man (7) ، groff (7) |
| 8 | أوامر إدارة النظام (عادةً للجذر فقط) |
| 9 | إجراءات Kernel [غير قياسية] |

## مثال - كيف تقرأ صفحات الرجل؟

فيما يلي مثال على كيفية استرداد المعلومات حول أمر MkDir باستخدام الأمر Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## مراجع

* [المواصفات الفنية لـ OpenDocument - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man (1) - صفحة دليل Linux] (https://man7.org/linux/man-pages/man1/man.1.html)

