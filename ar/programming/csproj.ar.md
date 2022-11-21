{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ" ,
  "description":"تعرف على تنسيق ملف CSPROJ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CSPROJ وفتحها." ,
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-05-21"
}

## ما هو ملف CSProj؟
تمثل الملفات ذات الامتداد CSPROJ ملف مشروع C # يحتوي على قائمة بالملفات المضمنة في المشروع بالإضافة إلى مراجع تجميعات النظام. عند بدء مشروع جديد في Microsoft VIiual Studio ، تحصل على ملف .csproj واحد مع ملف الحل الرئيسي ([.sln] (/ar/ architecture / sln /)). إذا كان هناك أكثر من تجميع واحد في المشروع ، فسيكون هناك عدد متساوٍ من ملفات المشروع بالإضافة إلى حيث يربطها ملف .sln معًا كجزء من المشروع. تحدد محتويات هذا الملف جميع المتطلبات المطلوبة لبناء المشروع مثل المحتوى المراد تضمينه ومتطلبات القاعدة ومعلومات الإصدار وخادم الويب أو إعدادات خادم قاعدة البيانات والمهام التي يجب تنفيذها. محتويات ملف المشروع مرتبة بتنسيق ملف XML ويمكن فتحها في أي محرر نصوص للتحرير والعرض. كما أنه يعطي رؤية منطقية لملفات المشروع من أجل الترتيب الصحيح.

## تنسيق ملف CSPROJ #

يمكن للمطورين إنشاء ملفات المشروع بأنفسهم وكذلك تكريم [MSBuild XML Schema] (https://msdn.microsoft.com/library/5dy88c2e.aspx). يتيح الهيكل المفتوح والشفاف لملفات المشروع لمطوري التطبيقات فرض تحكم متطور ودقيق في كيفية إنشاء المشاريع ونشرها. تحتوي محتويات ملف المشروع هذا على علاقة واضحة جدًا فيما بينها. يوضح الشكل التالي العناصر الأساسية والعلاقة بينها لملف المشروع.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

توضح الأقسام التالية بالتفصيل عناصر تنسيق الملف لملف المشروع.

### عنصر المشروع ###

عنصر [مشروع] (https://msdn.microsoft.com/library/bcxfsh87.aspx) هو العنصر الجذر لكل ملف مشروع. يحدد مخطط XML لملف المشروع ويمكن أن يتضمن سمات لتحديد نقاط الدخول لعملية البناء.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### الخصائص والشروط

تمثل الخصائص المعلومات الضرورية المطلوبة لبناء المشروع. يتم تحديد هذه الخصائص داخل عنصر [PropertyGroup] (https://msdn.microsoft.com/library/t4w159bs.aspx). تتكون هذه الخصائص من أزواج مفتاح - قيمة حيث يحدد اسم عنصر الخاصية مفتاح الخاصية ويحدد محتوى العنصر قيمة الخاصية. على سبيل المثال ، يمكنك تحديد الخصائص المسماة ServerName و ConnectionString لتخزين اسم خادم ثابت وسلسلة اتصال.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

يمكن تحديد الشروط من خلال العناصر من أجل تحديد معايير تقييم العنصر. يتم تحديد ذلك من خلال كلمة الشرط أثناء تحديد الخاصية كما هو موضح أدناه:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

عندما يعالج MSBuild تعريف الخاصية هذا ، فإنه يتحقق أولاً لمعرفة ما إذا كانت قيمة خاصية ** $ (OutputRoot) ** متاحة. إذا كانت قيمة الخاصية فارغة - بمعنى آخر ، لم يقدم المستخدم قيمة لهذه الخاصية - يتم تقييم الشرط إلى ** صحيح ** ويتم تعيين قيمة الخاصية على ** .. \ Publish \ Out. **

### العناصر ومجموعات العناصر

يعرّف ملف المشروع مدخلات عملية الإنشاء التي هي في الواقع أنواع ملفات مختلفة. في تسمية MSBuild ، يتم تمثيل هذه المدخلات بواسطة عناصر العنصر ويتم تعريفها داخل عنصر [ItemGroup] (https://msdn.microsoft.com/library/646dk05y.aspx). تمامًا مثل ** عناصر الخاصية ** ، يمكنك تسمية عنصر ** عنصر ** كيفما تشاء. ومع ذلك ، يجب عليك تحديد سمة ** Include ** لتعريف الملف أو حرف البدل الذي يمثله العنصر.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### الأهداف والمهام

يمثل عنصر [مهمة] (https://msdn.microsoft.com/library/77f2hx1s.aspx) تعليمة بناء فردية (أو مهمة). يتضمن MSBuild العديد من المهام المحددة مسبقًا. فمثلا:

* تنسخ المهمة ** Copy ** الملفات إلى موقع جديد.
* تستدعي مهمة ** Csc ** مترجم Visual C #.
* تستدعي المهمة ** Vbc ** مترجم Visual Basic.
* تقوم المهمة ** Exec ** بتشغيل برنامج محدد.
* تكتب مهمة ** الرسالة ** رسالة إلى المسجل.

يجب أن يتم احتواء المهام دائمًا داخل عناصر [الهدف] (https://msdn.microsoft.com/library/t50z2hka.aspx). عنصر ** الهدف ** هو مجموعة من مهمة واحدة أو أكثر يتم تنفيذها بالتتابع ، ويمكن أن يحتوي ملف المشروع على أهداف متعددة.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## مراجع

* [Understanding the Project File - MSDN] (https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- ملف)

