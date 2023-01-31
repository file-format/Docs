{
  "date" : "2021-04-08",
  "keywords" :["ملف deb" , "تنسيق ملف deb" , "ما هو ملف deb" , "ملف" , "deb example" , "امتداد ملف deb" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"تعرف على تنسيق ملف DEB وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DEB وفتحها." ,
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-09"
}

## ما هو ملف DEB؟

الملف بامتداد .deb هو تنسيق ملف حزمة ثنائي دبيان متاح لتوزيع حزم البرامج على نظام التشغيل Linux. يتكون من ملفي أرشيف [TAR] (/ar/ compression / tar /). توفر DPKG آلية لقراءة حزم DEB وتثبيتها. يمكن تثبيت حزم DEB باستخدام واجهة إدارة برامج حزمة APT. تحتوي ملفات DEB على نوع وسائط الإنترنت كـ `application / vnd.debian.binary-package`.

## تنسيق ملف DEB

يتكون ملف DEB من ملفي أرشيف [TAR] (/ar/ compression / tar /). يحتوي أحد الأرشيفات على معلومات التحكم والآخر يحتوي على البيانات القابلة للتثبيت.

### تنظيم الحزم

ملف DEB هو ملف أرشيف ** ar ** له قيمة سحرية هي `!<arch> ". منذ دبيان 0.93 ، آلية أرشفة ملفات DEB تحتوي على ثلاثة ملفات بترتيب معين.

1. "Debian Binary" - مقدّر له أن يحتوي على سلسلة من الأسطر ، مفصولة بأسطر جديدة. في الوقت الحاضر ، يوجد سطر واحد فقط يصف رقم الإصدار. رقم الإصدار الحالي هو 2.0.
1. "أرشيف التحكم" - يحتوي على أرشيف control.tar يحتوي على نصوص برمجية للمشرف ومعلومات وصفية حول الحزمة مثل اسم الحزمة والإصدار والتبعيات والمشرف.
1. "أرشيف البيانات" - هو أرشيف tar يسمى data.tar ويحتوي على ملفات الوسائط الفعلية القابلة للتثبيت. يمكن ضغط الأرشيف باستخدام gz أو bz2 أو lzma أو xz ، ويتغير امتداد ملف أرشيف البيانات وفقًا لذلك.

### أرشيف التحكم

يمكن أن يتضمن أرشيف التحكم محتويات على النحو التالي.

* `control` - يحتوي على وصف موجز للحزمة بالإضافة إلى معلومات أخرى مثل تبعياتها.
* `md5sums` - يحتوي على مجاميع اختبارية MD5 لجميع الملفات في الحزمة لاكتشاف الملفات التالفة أو غير المكتملة.
* `conffiles` - تسرد ملفات الحزمة التي يجب معاملتها كملفات تكوين. لا يتم الكتابة فوق ملفات التكوين أثناء التحديث ما لم يتم تحديد ذلك.
* `preinst` و postinst و prerm و postrm - البرامج النصية الاختيارية التي يتم تنفيذها قبل أو بعد تثبيت الحزمة أو إزالتها
* `config` هو برنامج نصي اختياري يدعم آلية تكوين debconf.
* "shlibs" - قائمة تبعيات المكتبة المشتركة.

## مراجع

* [DEB - Wikipedia] (https://en.wikipedia.org/wiki/Deb_ (file_format))
* [تنسيق حزمة دبيان الثنائية] (https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)
