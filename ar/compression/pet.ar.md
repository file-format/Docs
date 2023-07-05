{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف PET - ملف حزمة تثبيت Puppy Linux" ,
  "description":"تعرف على تنسيق ملف PET وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PET وفتحها." ,
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
} ,
  "lastmod" : "2022-06-23"
}

## ما هو ملف Linux PET؟

ملف PET هو ملف حزمة تثبيت تطبيق تم إنشاؤه واستخدامه مع متغير PuppyLinux لنظام التشغيل Linux. يتم إنشاؤه كملف مضغوط [TGZ](/ar/compression/tgz/) مما يقلل من حجم ملف الأرشيف المضغوط. يتم ضمان تكامل تنسيق ملف PET بواسطة المجموع الاختباري md5sum الذي يتم إلحاقه بنهاية الملف للتحقق منه في النهاية البعيدة. يمكن استخراج ملفات PET باستخدام مستخرج ملفات TGZ القياسي و WinRAR. استبدلت ملفات PET ملفات تثبيت حزمة [PUP](/ar/compression/pup/) القديمة.

## تنسيق ملف PET

يتم حفظ ملفات PET على القرص كأرشيفات مضغوطة بتنسيق ملف ثنائي. ومع ذلك ، فإن تفاصيل تنسيق الملف الداخلي لتنسيق ملف PET غير معروفة. على غرار ملفات تثبيت الحزمة [.exe](/ar/executable/exe/) و [.msi](/ar/executable/msi/) ، تبدأ ملفات PET التثبيت عند تنفيذها.

## مراجع

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [فهرس حزم PuppyLinux PET](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

