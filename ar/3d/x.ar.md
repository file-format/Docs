{
  "date" : "2020-01-11",
  "keywords" :["ملف x" , "تنسيق ملف x" , "ما هو ملف x" , "ملف" , "x مثال" , "امتداد ملف x" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف X - DirectX 2.0" ,
  "description":"تعرف على تنسيق ملف DirectX X وواجهات برمجة التطبيقات التي يمكنها فتح ملفات DirectX X وإنشاؤها." ,
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2020-01-11"
}

## ما هو ملف X؟

يشير ملف بامتداد .x إلى [DirectX] (https://www.microsoft.com/en-us/download/search.aspx؟q=directx) تنسيق ملف رسومات ثلاثي الأبعاد قديم تم تقديمه مع Microsoft DirectX 2.0. تم استخدامه لعرض الرسومات ثلاثية الأبعاد في الألعاب وتحديد هياكل الشبكات والأنسجة والرسوم المتحركة والكائنات المحددة من قبل المستخدم. لقد تم إهماله منذ عام 2014 حيث أن تنسيق ملف Autodesk FBX يعمل بشكل أفضل كتنسيق أكثر حداثة. X يعتمد على القوالب وخالي من أي معرفة بالاستخدام.

يمكنك فتح ملفات DirectX X باستخدام Microsoft DirectX وبرامج تحرير النصوص الشائعة.

## تنسيق ملف X

يحتوي [مرجع ملف X] (https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) على معلومات مرجعية لعناصر واجهة برمجة التطبيقات المستخدمة في العمل مع ملفات DirectX .x. يوفر التنسيق أساسيات بيانات منخفضة المستوى تستخدمها التطبيقات الأخرى لتحديد العناصر الأولية ذات المستوى الأعلى من خلال قوالب البيانات. قدم DirectX 6.0 واجهات وأساليب تمكن من القراءة من ملفات .x والكتابة إليها. قدم DirectX 3.0 إصدارًا ثنائيًا من تنسيق الملف هذا.

يحتوي [مرجع تنسيق ملف X] (https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) المحدد بواسطة DirectX 9 على معلومات مرجعية لـ .x الملفات في الترميز الثنائي وكذلك النص.

### الترميز الثنائي

يحدد [التنسيق الثنائي] (https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) تنسيق DirectX X باعتباره تمثيلًا مميزًا لتنسيق النص. يمكن أن تكون هذه الرموز المميزة قائمة بذاتها لإعطاء بنية نحوية أو يمكن أن تكون رموزًا تحمل سجلًا توفر البيانات اللازمة.

#### العنوان

يمكن قراءة الرأس الثنائي والكتابة باستخدام التعريفات التالية.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### ترميز النص

لا تعتمد ملفات DirectX .x على طريقة استخدام الملف وليست خاصة بأي تطبيق. يسمح هذا الأسلوب المستند إلى القوالب باستخدام تنسيق ملف .x بواسطة أي تطبيق عميل.


#### العنوان

الرأس متغير الطول إلزامي ويجب أن يكون في بداية تدفق البيانات. يحتوي العنوان على البيانات التالية.

| النوع | النوع الفرعي | الحجم | المحتويات | معنى المحتوى |
---|---|---|---|---|
| الرقم السحري (مطلوب) | | 4 بايت | xof |
| رقم الإصدار (مطلوب) | الرقم الأساسي | 2 بايت | 03 | الإصدار الرئيسي 3 |
| | رقم ثانوي | 2 بايت | 02 | الإصدار الثانوي 2 |
| نوع التنسيق (مطلوب) | | 4 بايت | "txt" | ملف نصي |
| | | | "بن" | ملف ثنائي |
| | | | "tzip" | ملف نصي مضغوط MSZip |
| | | | "bzip" | ملف ثنائي مضغوط MSZip |
| حجم الطفو (مطلوب) | | 4 بايت | 0064 | يطفو 64 بت |
| | | | 0032 | عوامات 32 بت |


## مراجع

* [X Files Legacy] (https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [مرجع تنسيق ملف DirectX 9] (https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

