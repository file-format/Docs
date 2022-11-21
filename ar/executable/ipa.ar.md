{
  "date" : "2021-08-30",
  "keywords" :["ipa file", "ipa file format", "what is a ipa file", "file", "ipa example", "ipa file extension", "extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف IPA وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات IPA وفتحها." ,
  "title" :"IPA - ملف حزمة تطبيق iOS" ,
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
} ,
  "lastmod" : "2021-08-30"
}

## ما هو ملف IPA؟
ينتمي ملف بامتداد .ipa إلى نظام التشغيل iOS ويعرف باسم ملف حزمة التطبيق. هذا ملف أرشيف (مضغوط باستخدام [ZIP] (/ar/ ضغط / zip /) ملف يخزن تطبيق iOS ، ولكن لا يمكن تثبيت هذا التطبيق إلا على أجهزة MacOS المستندة إلى iOS أو ARM ، مثل iPad أو iPhone أو لمس الآيبود. بشكل أساسي ، يمكن استخدام iTunes أو Apple Configurator 2 أو أي برنامج تابع لجهة خارجية لتثبيت ملفات IPA.

## تنسيق ملف IPA
مطورو IOS الذين يطورون التطبيقات باستخدام Apple Xcode على دراية بملفات IPA لأنهم يحتاجون إلى حزم تطبيقاتهم المطورة كملفات IPA إما لاختبار أغراض نشر متجر التطبيقات. على الرغم من أنه من المعروف أن ملفات IPA مثبتة كتطبيقات iOS ، إلا أنه يمكنك أيضًا فك ضغطها لعرض بيانات التطبيق الواردة. نظرًا لأن ملف IPA يحتوي على ثنائي واحد فقط لبنية ARM للهواتف المحمولة ولا يحتوي على ثنائي لمعمارية x86 ، فلا يمكن تثبيت العديد من ملفات .ipa على iPhone Simulator.
### بنية ملف .ipa
يوضح المثال التالي بنية IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
ما ورد أعلاه عبارة عن هيكل مدمج يتعرف عليه iTunes و App Store. حسب هذا الهيكل:
- يحتوي دليل Payload على جميع بيانات التطبيق.
- ملف iTunes Artwork هو صورة PNG بحجم 512 × 512 بكسل ، يحتوي على أيقونة التطبيق للعرض في iTunes وتطبيق App Store على iPad.
- يحتوي iTunesMetadata.plist على أجزاء مختلفة من المعلومات ، بدءًا من اسم المطور ومعرفه ، ومعلومات حقوق النشر ، ومعرف الحزمة ، واسم التطبيق ، والنوع ، وتاريخ الإصدار ، وتاريخ الشراء ، وما إلى ذلك.
- يحتوي مجلد META-INF فقط على بيانات وصفية حول البرنامج الذي تم استخدامه لإنشاء IPA.


## مراجع

* [.ipa - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/.ipa)


