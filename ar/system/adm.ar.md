{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ملف ADM - تنسيق ملف القالب الإداري",
  "description":"تعرف على تنسيق ملف ADM وكيفية فتح ملفات ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## ما هو ملف ADM؟

ملف ADM هو ملف قالب يستخدمه برنامج Microsoft Group Policies لتحديد موقع إعدادات السياسة المستندة إلى التسجيل في ملف التسجيل. يتم استخدامه من قبل مسؤولي النظام لتحديد سياسة إدارة مجموعة من أجهزة الكمبيوتر التي تشكل جزءًا من المجموعة. تصبح هذه المعلومات جزءًا من كائنات نهج المجموعة (GPOs) التي تم إنشاؤها لإدارة المجموعة.

يمكنك فتح ملفات ADM باستخدام محرر كائنات نهج المجموعة لـ Microsoft.

## تنسيق ملف ADM - مزيد من المعلومات

يتم تخزين ملفات ADM كملفات نصية بتنسيق Unicode. تم استخدامها بشكل أساسي لتحديد موقع إعدادات السياسة المستندة إلى التسجيل في سجل Windows Vista وWindows 7.

لم تعد ملفات ADM مدعومة وتم استبدالها بملفات [ADMX](/ar/system/admx/). يتجاهل GPA ملفات ADM الافتراضية التالية على أجهزة الكمبيوتر التي تعمل بنظام التشغيل Microsoft Windows Vista Service Pack 1 أو الإصدارات الأحدث.

* نظام.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## مراجع

* [ملفات النماذج الإدارية - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - إدارة ملفات القوالب الإدارية](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

