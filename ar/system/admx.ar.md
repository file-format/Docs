{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ملف ADMX - تنسيق ملف القالب الإداري لنهج المجموعة",
  "description":"تعرف على تنسيق ملف ADMX وكيفية فتح ملفات ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## ما هو ملف ADMX؟

ملف ADMX هو ملف تكوين سياسة يستخدمه برنامج Microsoft Windows Group Policy الذي يدير مجموعة من أجهزة الكمبيوتر في مجموعة. وهو عبارة عن ملف قالب إداري يستند إلى XML وتم تقديمه مع Windows Vista Service Pack 1. تحتوي ملفات ADMX على إعدادات التكوين لحسابات المستخدمين وتكوينات نظام التشغيل والتطبيقات. تُستخدم ملفات ADMX لتخزين ونشر التكوينات للإدارة المركزية للعديد من أنظمة الكمبيوتر.

يمكنك إنشاء ملفات ADMX أو تحريرها باستخدام أي محرر نصوص متوافق مع XML أو محرر كائنات نهج المجموعة من Microsoft.

## تنسيق ملف ADMX - مزيد من المعلومات

يتم تخزين ملفات ADMX بتنسيق ملف [XML](/ar/web/xml/) العالمي الذي يمكن قراءته بواسطة الإنسان. إنه تنسيق ملف متعدد اللغات ويسمح لمسؤولي النظام من لغات مختلفة بالعمل مع نفس ملفات ADMX. استبدلت ملفات ADMX تنسيق الملف القديم [ADM](/ar/system/adm/) وهو تنسيق ملف نصي بتنسيق Unicode. تحدد ملفات ADMX مفاتيح التسجيل التي يتم تغييرها عند تغيير إعداد "نهج المجموعة" معين.

### ماذا يمكنني أن أفعل بملف ADMX؟

تحدد ملفات ADMX الإجراءات التي سيتم السماح بها لأجهزة كمبيوتر المستخدم التي تشكل جزءًا من مجموعة. تفرض سياسة المجموعة القواعد المحددة مع برنامج Active Directory. تتم إدارة ملفات ADMX من المتجر المركزي على نظام التشغيل Windows والذي يعد موقعًا مركزيًا في المجال.

يمكن لملف ADMX الذي تم نشره في بيئة العمل أن يسمح للمسؤولين بتنفيذ سياسات مثل:

* التحكم في استخدام الانترنت
* تنزيل أنواع معينة من الملفات
* استخدام الأجهزة القابلة للإزالة على الأنظمة

## مراجع

* [ملفات النماذج الإدارية - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - إدارة ملفات القوالب الإدارية](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

