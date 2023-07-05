{
  "date" : "2021-04-08",
  "keywords" :["rpm file", "rpm file format", "what is a rpm file", "file", "rpm example", "rpm file extension", "extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - ملف Red Hat Package Manager" ,
  "description":"تعرف على تنسيق ملف RPM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RPM وفتحها." ,
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-09"
}

## ما هو ملف RPM؟

الملف بامتداد .rpm هو حزمة نظام تشغيل Red Hat Linux لتثبيت البرامج على أنظمة Linux. يستخدم Red Hat Package Manager تنسيق ملف RPM وهو نظام إدارة حزم مجاني ومفتوح المصدر. على الرغم من أنه يمكن استخدام ملفات RPM كما هو الحال في تثبيت البرامج ، إلا أنه يمكن تحويلها إلى تنسيقات حزم أخرى مثل [DEB](/ar/compression/deb/) باستخدام برنامج Debian المسمى Alien.

## تنسيق ملف RPM

ملف RPM هو ملف ثنائي يمكن أن يحتوي على مجموعة من الملفات. في معظم الأحيان ، تكون ملفات RPM "RPMs ثنائية" وهي الملفات التنفيذية المترجمة للبرنامج. يمكن أن يحتوي ملف RPM على RPMs المصدر (SRPMs) التي يمكن استخدامها لإنشاء الحزمة من التعليمات البرمجية المصدر. يتكون تنسيق ملف RPM من أربعة أقسام.

* الرصاص - يحدد الملف كملف RPM
* التوقيع - يمكن استخدامه لضمان النزاهة و / أو الأصالة
* الرأس - يحتوي على بيانات وصفية بما في ذلك اسم الحزمة ، والإصدار ، والهندسة المعمارية ، وقائمة الملفات ، وما إلى ذلك.
* أرشيف الملفات - يُعرف أيضًا باسم الحمولة ، والتي تكون عادةً بتنسيق cpio ، مضغوطة باستخدام [GZIP](/ar/compression/gz/)

## مراجع

* [RPM - Wikipedia](https://rpm.org)
* [وثائق RPM](https://rpm.org/documentation.html)

