{
  "date" : "2019-10-11",
  "keywords" :[".swf" , "SWF" , "Apple swift" , "file" , "extension" , "تنسيق الملف" , "برنامج apple swift التعليمي" , "دليل البرمجة"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SWIFT - ملف رمز مصدر Apple" ,
  "description":"تعرف على تنسيق ملف SWIFT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SWIFT وفتحها." ,
  "linktitle" : "SWIFT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف Swift؟

يشير ملف بامتداد .swift إلى لغة برمجة SWIFT التي قدمتها Apple لكتابة تطبيقات وتطبيقات البرامج لنظام التشغيل macOS و iOS و tvOS وما بعده. قبل SWIFT ، كانت Objective-C هي لغة البرمجة الرئيسية لكتابة التطبيقات. يمكن استخدامه مع Xcode وهي مجموعة أدوات مطور كاملة لإنشاء تطبيقات لأجهزة Mac و iPhone و iPad و Apple Watch و Apple TV. تعد SWIFT أكثر قوة وتفاعلية وتعبيرًا وتوفر المزيد من الأمان حسب التصميم دون المساومة على الأداء. يمكن فتح ملفات Swift للتحرير في أي محرر نصوص بالإضافة إلى Apple Xcode. وهو يدعم أنظمة تشغيل Apple و Linux و Windows و Android.

## نبذة تاريخية

* بدأ التطوير في منتصف عام 2010 بواسطة Chris Lattner بمساهمة من مبرمجين آخرين من Apple
* تم إصدار أول تطبيق رسمي مكتوب بلغة SWIFT في 2 يونيو 2014 في مؤتمر مطوري Apple WorldWide (WWDC) وتم إصدار إصدار تجريبي من اللغة لمطوري Apple المسجلين
* تم إصدار Swift 1.0 في 9 سبتمبر 2014 باستخدام Xcode لنظام iOS
* تم إصدار Swift 1.1 في 22 أكتوبر 2014 مع إطلاق Xcode 6.1
* تم إصدار Swift 1.2 في 8 أبريل 2015 ، إلى جانب Xcode 6.3
* تم الإعلان عن Swift 2.0 في WWDC 2015 ، وتم إتاحته لنشر التطبيقات في App Store في 21 سبتمبر 2015.
* تم إصدار Swift 3.0 في 13 سبتمبر 2016.
* تم إصدار Swift 4.0 في 19 سبتمبر 2017.
* تم إصدار Swift 4.1 في 29 مارس 2018.
* كانت لغة Swift مفتوحة المصدر في 3 ديسمبر 2015 جنبًا إلى جنب مع المكتبات الداعمة ومصحح الأخطاء ومدير الحزم بموجب ترخيص Apache 2.0. تمت استضافة المشروع على [Swift.org] (https://swift.org/) ويتم استضافة كود المصدر الخاص به على [GitHub] (https://github.com/apple/swift).
* خلال WWDC 2019 ، أعلنت Apple عن إطار عمل SwiftUI لتصميم هيكل واجهة المستخدم عبر جميع منصات Apple

## تنسيق ملف سريع - مزيد من المعلومات

ملفات Swift هي ملفات نصية عادية يمكن فتحها باستخدام أي محرر نصوص. محرر النصوص الأساسي المستخدم لفتح وتحرير الملفات السريعة هو Xcode من Apple. العديد من أجزاء Swift مألوفة لتطوير التطبيقات باستخدام C و Objective-C. توفر وثائق Swift [دليل تطوير التطبيق] مفصلًا (https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html) لكتابة التعليمات البرمجية باستخدام Swift.

## ميزات اللغة السريعة

يتميز Swift عن لغات البرامج الأخرى بناءً على الميزات التالية.

"حديث" - يتم التعبير عن المعلمات المسماة بصيغة نظيفة تجعل من السهل قراءة وصيانة واجهات برمجة التطبيقات في Swift. والأفضل من ذلك ، أنك لا تحتاج حتى إلى كتابة الفاصلة المنقوطة.

"الأمان" - دائمًا ما تتم تهيئة المتغيرات قبل الاستخدام ، ويتم فحص المصفوفات والأعداد الصحيحة للتحقق من التدفق الزائد ، وتتم إدارة الذاكرة تلقائيًا ، وفرض الوصول الحصري إلى حراس الذاكرة ضد العديد من أخطاء البرمجة.

"سريع وقوي" - باستخدام تقنية مترجم LLVM عالية الأداء بشكل لا يصدق ، يتم تحويل كود Swift إلى كود أصلي محسّن يحقق أقصى استفادة من الأجهزة الحديثة.

"التوافق مع المصدر والثنائي" - التطبيقات التي تم تطويرها باستخدام الإصدار السابق من Swift متوافقة مع الإصدارات الجديدة ولا يلزم إعادة ترجمة التعليمات البرمجية المصدر. مع إطلاق Swift 5 ، يتم تضمين مكتبات Swift في كل إصدار من أنظمة التشغيل من الآن فصاعدًا. يؤدي ذلك إلى تجنب تضمين مكتبات Swift في التطبيقات التي تستهدف إصدارات نظام التشغيل الحالية والمستقبلية.

"المصدر المفتوح" - Swift مفتوح المصدر مع مئات المساهمات من أعضاء مجتمع Swift. إنه مدعوم بمتعقب أخطاء قوي ومنتديات وإنشاءات تطوير منتظمة متاحة للجمهور للجميع.

## مراجع
* [Swift - GitHub] (https://github.com/apple/swift)
* [سويفت - ويكيبيديا] (https://en.wikipedia.org/wiki/Swift_ (architecture_language))
