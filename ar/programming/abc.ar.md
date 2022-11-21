
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ملف كود ActionScript Byte Code" ,
  "description":"تعرف على ما هو تنسيق ملف ABC مع أمثلة وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ABC وفتحها." ,
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-12-14"
}

## ما هو ملف ABC؟

الملف ذو الامتداد .abc هو ملف أكشن سكريبت بايت كود تم إنشاؤه بواسطة مترجم فلاش كنتيجة لتجميع ملفات البرنامج النصي أكشن سكريبت. يتم تنفيذ كود البايت الموجود في ملف ABC بواسطة ActionScript Virtual Machine (AVM و AVM2). يتكون رمز البايت من بيانات ثابتة وإرشادات من مجموعة تعليمات AVM2 وأنواع مختلفة من البيانات الوصفية. عندما يتم تحميل ملف ABC في AVM أو AVM2 ، فإنه يخضع للتحقق. إذا كان لا يتوافق مع نظرة عامة على AVM2 ، فسيتم رفضه. يمكن فتح ملفات ABC في Adobe Flash Player الذي توقف منذ فترة طويلة.

## تنسيق ملف ABC - مزيد من المعلومات

يتم حفظ ملفات ABC على القرص بتنسيق ملف ثنائي يمكن قراءته بواسطة الأجهزة الظاهرية AVM أو AVM2. يمثل هيكل الملف الداخلي الخاص به كتلة التعليمات البرمجية القابلة للتنفيذ بكل بياناته الثابتة ، واصفات النوع ، والكود ، والبيانات الوصفية.

## هيكل ملف ABC

هيكل ملف ABC كما هو موضح أدناه.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### حقول ملفات ABC

| اسم الحقل | الوصف |
---|---|
| Minor_version، major_version | إن قيم major_version و Secondary_version هي أرقام الإصدارات الرئيسية والثانوية من تنسيق abcFile.
| ثابت_بول | ثابت_بول عبارة عن بنية متغيرة الطول تتكون من أعداد صحيحة ومضاعفات وسلاسل ومساحات أسماء ومجموعات مساحة الاسم وأسماء متعددة.
| method_count ، الطريقة | قيمة الطريقة هي عدد الإدخالات في مصفوفة الأسلوب. كل إدخال في مصفوفة الأسلوب هو بنية معلومات طريقة متغيرة الطول
| metadata_count ، metadata | قيمة metadata_count هي عدد الإدخالات في مصفوفة البيانات الوصفية. كل إدخال للبيانات الوصفية هو metadata_infostructure الذي يعيّن اسمًا لمجموعة من قيم السلسلة. |
| class_count ، example ، class | قيمة class_count هي عدد الإدخالات في مصفوفات المثيل والفئة. |
| script_count ، script | قيمة script_count هي عدد الإدخالات في مصفوفة البرنامج النصي. كل إدخال نصي هو بنية script_info تحدد خصائص برنامج نصي واحد في هذا الملف. |
| method_body_count ، method_body | قيمة method_body_count هي عدد الإدخالات في مصفوفة method_body. يتكون كل method_bodyentry من بنية method_body_info متغيرة الطول تحتوي على تعليمات لطريقة أو وظيفة فردية.

## مراجع

* [Robust ABC (ActionScript Bytecode) [Dis-] Assembler - Github] (https://github.com/CyberShadow/RABCDAsm)

