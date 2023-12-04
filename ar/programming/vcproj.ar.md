{
"التاريخ": "15-05-2023",
  "keywords": [
"ملف vcproj",
"ما هو ملف vcproj",
"مثال على ملف vcproj",
"ماذا يحتوي ملف vcproj",
"ما هو تنسيق ملف vcproj",
"ملف",
"امتداد الملف vcproj",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
"title": "تنسيق ملف VCPROJ - ملف مشروع Visual C++",
  "description":"تعرف على تنسيق VCPROJ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VCPROJ وفتحها.",
"linktitle": "VCPROJ",
  "menu": {
    "docs": {
      "identifier": "programming-vcproj",
"parent" : "programming"
}
},
"آخر مود": "15-05-2023"
}

## ما هو ملف VCPROJ؟

ملف VCProj, المعروف أيضًا باسم ملف مشروع Visual C++, هو ملف يستند إلى XML يقوم بتخزين التكوين والإعدادات للمشروع في Microsoft Visual Studio. تُستخدم ملفات VCProj بشكل أساسي في الإصدارات الأقدم من Visual Studio, حتى Visual Studio 2010. بدءًا من Visual Studio 2012, تم تغيير ملفات المشروع إلى تنسيق جديد يسمى VCXProj.

يحتوي ملف VCProj على معلومات حول ملفات التعليمات البرمجية المصدر للمشروع وإعدادات البناء وخيارات المترجم وإعدادات الرابط والتكوينات الأخرى الخاصة بالمشروع. فهو يحدد كيفية بناء المشروع وما هي الملفات المضمنة في المشروع.

## مثال لملف VCPROJ

فيما يلي مثال لما قد يبدو عليه ملف VCProj:

```
<?xml version="1.0" encoding="Windows-1252"?>
<VisualStudioProject
	ProjectType="Visual C++"
	Version="9.00"
	Name="MyProject"
	ProjectGUID="{01234567-89AB-CDEF-0123-456789ABCDEF}"
	Keyword="Win32Proj"
	>
	<Platforms>
		<Platform
			Name="Win32"
		/>
	</Platforms>
	<ToolFiles>
	</ToolFiles>
	<Configurations>
		<Configuration
			Name="Debug|Win32"
			ConfigurationType="1"
			InheritedPropertySheets="$(VCInstallDir)VCProjectDefaults\UpgradeFromVC71.vsprops"
		>
			<Tool
				Name="VCCLCompilerTool"
				AdditionalIncludeDirectories=".\include"
				PreprocessorDefinitions="_DEBUG;WIN32;_WINDOWS"
				RuntimeLibrary="3"
				UsePrecompiledHeader="0"
			/>
			<Tool
				Name="VCLinkerTool"
				AdditionalDependencies="kernel32.lib user32.lib"
				OutputFile="$(OutDir)\MyProject.exe"
				LinkIncremental="2"
				SuppressStartupBanner="true"
			/>
		</Configuration>
	</Configurations>
	<References>
	</References>
</VisualStudioProject>

```

## ماذا يحتوي ملف VCPROJ؟

يحتوي ملف VCProj على عناصر وإعدادات متنوعة تتعلق بمشروع Visual C++ في Microsoft Visual Studio. فيما يلي بعض المعلومات الأساسية التي يمكن العثور عليها في ملف VCProj:

- **معلومات المشروع:** يتضمن ملف VCProj معلومات على مستوى المشروع مثل اسم المشروع ونوع المشروع والإصدار والمعرف الفريد (GUID) للمشروع.
- **المنصات والتكوينات:** تحدد الأنظمة الأساسية والتكوينات التي يدعمها المشروع. تحدد الأنظمة الأساسية النظام الأساسي المستهدف, مثل Win32 أو x64 أو ARM, بينما تحدد التكوينات تكوينات بناء مختلفة مثل Debug أو Release.
- **ملفات المصدر:** يسرد ملف VCProj ملفات التعليمات البرمجية المصدر التي تعد جزءًا من المشروع, بما في ذلك ملفات C++ وملفات الرأس وملفات الموارد والملفات الأخرى ذات الصلة. عادةً ما يتم تحديد كل ملف بمساره النسبي إلى دليل المشروع.
- **إعدادات البناء:** تتضمن الإعدادات المتعلقة بعملية البناء, مثل خيارات المترجم, وخيارات الرابط, وتعريفات المعالج المسبق, وأدلة التضمين الإضافية, والتبعيات الإضافية. تحدد هذه الإعدادات كيفية إنشاء المشروع وربطه.
- **الرؤوس المترجمة مسبقًا:** يمكن لملف VCProj تحديد ما إذا كان المشروع يستخدم الرؤوس المترجمة مسبقًا, وإذا كان الأمر كذلك, أي ملف يعمل كرأس مترجم مسبقًا.
- **معلومات الإخراج:** تحدد ملف الإخراج أو الملفات التي تم إنشاؤها بواسطة عملية الإنشاء, مثل الملف القابل للتنفيذ, أو مكتبة الارتباط الديناميكي (DLL), أو المكتبة الثابتة (LIB). يمكن تكوين مسار ملف الإخراج واسمه في ملف VCProj.
- **المراجع:** قد يحتوي ملف VCProj على مراجع لمشاريع أخرى أو مكتبات خارجية يعتمد عليها المشروع. تساعد هذه المراجع في حل التبعيات أثناء عملية الإنشاء.
- **خطوات البناء المخصصة:** إذا كان المشروع يتطلب خطوات بناء مخصصة إضافية, مثل تشغيل البرامج النصية أو تنفيذ أدوات خارجية, فيمكن أن يتضمن ملف VCProj تعليمات لهذه الخطوات.
- **التصحيح والنشر:** قد يتضمن ملف VCProj الإعدادات المتعلقة بالتصحيح والنشر والتكوينات الأخرى الخاصة بالمشروع.

## ما هو تنسيق ملف VCPROJ؟

يعتمد تنسيق ملف VCProj على XML (لغة التوصيف الموسعة), وهي لغة ترميز قياسية لتمثيل البيانات المنظمة. يسمح تنسيق XML بتنظيم وتخزين المعلومات والإعدادات الخاصة بالمشروع في هيكل هرمي.

## مراجع
* [ملفات المشاريع والحلول](https://learn.microsoft.com/en-us/cpp/build/reference/project-and-solution-files?view=msvc-170)

