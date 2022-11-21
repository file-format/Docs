{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SLN" ,
  "description":"تعرف على تنسيق ملف SLN وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SLN وفتحها." ,
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف SLN؟
يمثل الملف بامتداد .SLN ملف ** حل Visual Studio ** الذي يحتفظ بالمعلومات حول تنظيم المشاريع في ملف الحل. تتم كتابة محتويات ملف الحل هذا بنص عادي داخل الملف ويمكن ملاحظتها / تحريرها عن طريق فتح الملف في أي محرر نصوص. تظل المعلومات الواردة في ملف الحل ثابتة ويتم استخدامها لتحميل المعلومات المرتبطة بالحل مثل [المشاريع] (/ar/ البرمجة / csproj /) وأي معلومات أخرى مطلوبة. تحتوي ملفات المشروع المشار إليها بواسطة ملف الحل على معلومات إضافية لتمكين البيئة لملء التسلسل الهرمي بعناصر هذا المشروع. لا يتم تخزين أي بيانات في ملف .sln ، على الرغم من أنه يمكن كتابة معلومات المشروع في ملف .sln إذا لزم الأمر.

## ** تاريخ إصدارات SLN ** ##

تطور إصدار تنسيق الحل مع كل حل من حلول Microsoft Visual Studio بمرور الوقت. التفاصيل حول هذه هي كما يلي.


| إصدار Visual Studio | إصدار تنسيق الحل
---|---|
| 2003 | 8.00
| 2005 | 9.00
| 2008 | 10.00
| 2010 | 11.00
| 2013 | 12.00
| 2015 | 12.00
| 2017 | 12.00

### ** محتويات ملف الحل ** ###

يتكون ملف الحل من عدة أقسام تقرأها البيئة لتحميل المشروع. محتويات ملف .sln عينة كما هو موضح أدناه.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### ** إعلان المشروع ** ###

يمكن أن يحتوي ملف الحل على أكثر من إعلان مشروع واحد وكذلك اختلاف أنواع المشاريع. على سبيل المثال ، يمكن أن يحتوي ملف حل واحد على CSharp بالإضافة إلى مشروع VB.NET. يتم تمييز هذه الأنواع في حل باستخدام [Project-Type-GUID] (https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). يمكن تعميم إعلان المشروع أعلاه على النحو التالي لفهم واضح.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

Project-Type-GUID: يعتبر Project-Type-GUID فريدًا لأنواع المشاريع المختلفة ويستخدمه قارئ الحلول لتحديد نوع المشروع. في هذه الحالة ، يوضح F184B08F-C81C-45F6-A57F-5ABD9991F28F أنه مشروع VB.NET.

مشروع GUID: GUID الفريد للمشروع الذي يميزه عن المشاريع الأخرى في الحل. المعرف الفريد للمشروع في الحل يجعل من الممكن للمشاريع الأخرى في الحل الوصول إليه.

استنادًا إلى المعلومات الواردة في قسم المشروع من ملف .sln ، تقوم البيئة بتحميل كل ملف مشروع. ثم يكون المشروع نفسه مسؤولاً عن ملء التسلسل الهرمي للمشروع وتحميل أي مشاريع متداخلة. يتم حفظ أي تغييرات يتم إجراؤها على الحل مرة أخرى في ملف الحل عند حفظ المشروع أو إغلاقه.

## مشروع Visual Studio حل VS

** المشروع: ** منطقيًا ، عندما تبدأ في إنشاء تطبيق أو برنامج باستخدام Visual Studio ، فإنك تبدأ مشروعًا جديدًا. يحتوي المشروع على جميع الملفات الضرورية مثل الكود المصدري والرموز والصور وملفات البيانات والمزيد ، والتي سيتم تجميعها في تطبيق قابل للتنفيذ أو موقع ويب أو مكتبة.

** الحل: ** يحتوي الحل على مشروع واحد أو أكثر. لذا فإن الحل يشبه الحاوية لمشاريع Visual Studio. منطقيًا ، يمكننا القول إن شخصًا ما يريد الحصول على حل كامل لأعماله بما في ذلك موقع ويب وتطبيق سطح مكتب وخدمة مريحة وتطبيق جوال.

### **مراجع** ###

* [ملف الحل - بواسطة MSDN] (https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file؟view#vs-2017)
* [Project Type GUIDs] (https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

