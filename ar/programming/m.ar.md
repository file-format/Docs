{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف التعليمات البرمجية المصدر M - Matlab" ,
  "description":"تعرف على ملف Matlab .m Source Code و APIs التي يمكنها إنشاء ملفات MF وفتحها." ,
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

# M - ملفات كود مصدر ماتلاب

## ما هو ملف M (ماتلاب)؟

ملف بامتداد .m هو ملف شفرة مصدر يستخدمه Matlab ، وهو نظام أساسي للبرمجة والحساب الرقمي يستخدم للتحليل وتطوير الخوارزميات ونمذجة المحاكاة. مثل تنسيقات ملفات البرمجة الأخرى ، يحتوي ملف M على كود مصدر ينفذ أوامر Matlab لرسم الرسوم البيانية وتشغيل عمليات المحاكاة والعمليات الرياضية الأخرى. يمكن لمحاكاة Matlab الفردية أن تمتد عبر عدة ملفات .m التي يمكنها تصنيف التطبيق في البرامج النصية أو الفئات أو الوظائف أو الإعلانات. يمكن فتح ملفات Matlab M باستخدام أي محرر نصوص.

## تنسيق ملف Matlab M - مزيد من المعلومات

ملفات Matlab .m هي ملفات نصية تحتوي على كود برمجة في لغة برمجة Matlab. يمكن فتحها وتحريرها في أي محرر نصوص ، وحفظها مرة أخرى ليتم تنفيذها في برنامج Matlab. يحتوي Matlab نفسه على محرر مباشر يستخدم لإنشاء البرامج النصية التي هي مزيج من التعليمات البرمجية والإخراج والنص المنسق.

### ملفات وظائف ماتلاب

مثل لغات البرمجة الأخرى ، يمكنك إنشاء ملف .m يحتوي فقط على تعريف الوظيفة التي تؤدي مهمة معينة فقط. يتم أيضًا حفظ هذه الملفات بامتداد .m وتنفذ الوظائف المتعلقة بهذه الوظيفة فقط.

### مثال ملف M.

فيما يلي مثال لملف دالة Matlab يحسب الوقت المستغرق لكائن تم إسقاطه من ارتفاع h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

لاستدعاء هذه الوظيفة من محرر Matlab أو من ملف .m آخر ، يمكن استخدام الكود التالي.
```C++
TimeToGround(100)
```

## مراجع

* [ماتلاب - تنسيقات الملفات المدعومة](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [باستخدام Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - ملف تنفيذ الهدف- C

## ما هو ملف M (Objective-C)؟

يشار إلى ملف M أيضًا باسم ملف التنفيذ الذي يحتوي على كود مصدر لفئة مكتوبة بلغة Objective-C ، وهي لغة برمجة تُستخدم لكتابة تطبيقات برمجية لنظامي التشغيل OS X و iOS. Objective-C هي لغة البرمجة الرئيسية التي تستخدمها Apple APIs الرئيسية ، Cocoa و Cocoa Touch ، لهذه الأنظمة الأساسية. قد يحتوي تطبيق برمجي واحد تم تطويره بهذه اللغة على ملفات .m متعددة ، تحتوي على تنفيذ فئات البرنامج. يمكن فتحها باستخدام Apple XCode و jEdit وبرامج تحرير النصوص الشائعة الأخرى.

## تنسيق ملف Objective-C M - مزيد من المعلومات

تتم كتابة ملفات M بتنسيق نص عادي باستخدام بناء جملة البرمجة لـ Objective-C. يجب تعريف كل طريقة في الفصل بكل التعليمات البرمجية الضرورية في ملفات التنفيذ هذه. يمكن لملفات التنفيذ M استيراد ملف رأس واحد أو أكثر وفقًا للمتطلبات. يخبر بيان الاستيراد المترجم بمكان العثور على ملف الرأس الذي ينتمي إلى ملف التنفيذ هذا. بيان الاستيراد مكتوب على النحو التالي.

```C++
#import "network.h"
```

يبدأ كل تطبيق ملف M بعد ذلك بالتوجيه "@ التطبيق" ، متبوعًا باسم ملف فئة التنفيذ. ثم يتبع ذلك تنفيذ جميع الأساليب التي تم التصريح عنها في ملف الرأس.

### مثال تنسيق ملف M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## مراجع
* [حول الهدف C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [دليل الكائن C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

