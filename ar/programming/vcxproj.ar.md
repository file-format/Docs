{
  "date" : "2019-10-11",
  "keywords" :["vcxproj", "file", "extension", "file format", "Visual C ++ Project", "Programming Guide"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ" ,
  "description":"تعرف على تنسيق ملف VCXPROJ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VCXPROJ وفتحها." ,
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف VCXPROJ؟

الملف بامتداد vcxproj. هو ملف مشروع Microsoft Visual C ++ يخزن [C ++](/ar/programming/cpp/) معلومات المشروع. يحتوي على المعلومات التي يستخدمها نظام مشروع MSBuild لتجميع وبناء المخرجات النهائية. VCXPROJ لمشاريع Visual C ++ هو نفس برنامج [CSPROJ](/ar/programming/csproj/) لمشاريع .NET. لا تحتوي ملفات VCXPROJ على أي رمز ولكنها تشير إلى جميع الفئات والأهداف والخصائص المحددة للمشروع لبناء المشروع. يمكن فتحها في برامج تحرير النص العادي أو يفضل في Microsoft Visual Studio IDE.


## تنسيق ملف VCXPROJ - مزيد من المعلومات

ملفات VCXPROJ هي ملفات نصية تم إنشاؤها بتنسيق ملف [XML](/ar/web/xml/). يمكن فتحها في أي محرر نصوص ولكن يوصى بشدة باستخدام Microsoft Visual Studio IDE لفتح هذه الملفات وتحريرها. لم يتم تصميمها للتحرير اليدوي. يمكن أن تتسبب الأخطاء في تعطل IDE أو التصرف بطرق غير متوقعة.

محتويات نموذج ملف VCXPROJ كما يلي.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### عناصر ملف VCXPROJ

يحتوي ملف VCXPROJ النموذجي على عدد من العناصر كما يمكن رؤيته في مثال XML أعلاه. تشرح [بنية VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure؟view=msvc-160) بواسطة Microsoft كل عنصر ملف بالتفصيل ويمكن الرجوع إليه من منظور المطور.

#### عنصر المشروع

هذه هي العقدة الجذرية لملف VCXPROJ. يستخدم MSBuild هذا العنصر لقراءة إصدار البناء والهدف الافتراضي للترجمة.

#### ProjectConfigurations ItemGroup Element

يحتوي على معلومات تكوين المشروع التي يمكن أن تتضمن طريقة الإنشاء (التصحيح أو الإصدار) ، وتجميع 32 أو 64 بت ، وخيارات التحسين ، وغيرها. يتم استخدام المعلومات الموجودة في هذه المجموعة بواسطة IDE لتحميل المشروع.

#### عناصر تكوين المشروع

تحتوي عناصر ProjectConfiguration في ملف VCXPROJ على معلومات حول البنية والنظام الأساسي الذي تم تحميل المشروع من أجله. يجب أن يتبع اسمه التنسيق "$ (Configuration) | $ (Platform)`.

#### Globals PropertyGroup Element

يحتوي هذا القسم على الإعدادات التي توفر معلومات لمستوى المشروع مثل:

* دليل المشروع
* RootNamespace
* نوع التطبيق أو ApplicationTypeRevision


## مراجع

* [بنية VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure؟view=msvc-160)
* [ملفات مشروع C ++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files؟view=msvc-160)

