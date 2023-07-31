{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C ++ Resource File" ,
  "description":"تعرف على تنسيق ملف APS باستخدام مثال APS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات APS وفتحها." ,
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-04-22"
}

## ما هو تنسيق ملف APS؟
يتم إنشاء ملف APS بواسطة Visual C ++ ، وهو أحد تطبيقات تطوير البرامج بواسطة Microsoft. يحفظ التمثيل الثنائي لمورد مدمج مع المشروع ويسمح للتطبيق بتحميل الموارد بسرعة أكبر. يمكنك بسهولة العثور على هذه الملفات بامتداد ملف .aps. في الواقع ، لا يقوم محررو الموارد بقراءة ملفات Resource.h مباشرة وهذا هو السبب في أن مترجم المورد يجمعهم في ملفات .aps التي يستهلكها محررو الموارد.

## تنسيق ملف APS
يعد تنسيق ملف APS مجرد خطوة ترجمة ويخزن البيانات الرمزية فقط. يتم تجاهل المعلومات غير الرمزية مثل التعليق أثناء عملية الترجمة. على سبيل المثال ، عند الحفظ ، يكتب محرر المورد فوق ملف البرنامج النصي للمورد وملف Resource.h. تظل أي تغييرات تطرأ على الموارد نفسها مدمجة في ملف البرنامج النصي للمورد ، ولكن التعليقات ستفقد دائمًا بمجرد الكتابة فوق ملف البرنامج النصي للمورد.


## مراجع

* [Resource Files (C ++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio؟view=msvc-160)
 


