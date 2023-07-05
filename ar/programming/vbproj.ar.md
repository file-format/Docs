{
  "date" : "2019-10-11",
  "keywords" :["vbproj", "file", "extension", "file format", "VB Project File", "Programming Guide"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"تعرف على تنسيق ملف VBPROJ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VBPROJ وفتحها." ,
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2020-09-10"
}

## ما هو ملف VBPROJ؟

الملف ذو الامتداد .vbproj هو ملف مشروع Microsoft Visual Basic يتم استخدامه بواسطة محرك Microsoft MSBuild لبناء المشاريع ضمن حل Visual Studio. إنه مشابه لملف [CSPROJ](/ar/programming/csproj/) لمشاريع .NET المكتوبة في [C #](/ar/programming/cs/). يقوم محرك MSBuild بقراءة المعلومات الموجودة في مجموعات مختلفة من ملفات VBPROJ ويقوم بإنشاء ملف الإخراج. يمكن أن يحتوي ملف VBPROJ على معلومات تتعلق بالمعرفات والفئات والخصائص العامة التي تحدد المشروع. يمكن فتح ملفات VBPROJ وتحريرها باستخدام Microsoft Visual Studio وأي محرر نصوص شائع مثل Notepad على أنظمة تشغيل Windows و MacOS.

## تنسيق ملف VBPROJ - مزيد من المعلومات

ملفات VBPROJ هي ملفات نصية مكتوبة بتنسيق ملف [XML](/ar/web/xml/) بناءً على [MSBuild XML Schema](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild- مشروع-ملف-مخطط-مرجع؟ عرض = مقابل -2019). يحتوي ملف VBPROJ على معلومات في شكل علامات XML التي تحدد المعلومات المتعلقة بمجموعة الإعدادات المحددة. يوصى بشدة بفتح ملفات الإعداد هذه وتحريرها في Microsoft Visual Studio IDE.

### عناصر VBPROJ

العناصر المكونة لملف إعدادات VB موضحة في الصورة التالية.

{{< figure src="../vbproj.png" alt="تنسيق ملف VBPROJ" >}}

يقدم الجدول التالي وصفًا موجزًا لهذه العناصر.

| العنصر | الوصف |
---|---|
| مشروع | عنصر جذر لكل ملف مشروع ويمكن أن يتضمن سمات لتحديد نقاط الدخول لعملية الإنشاء بالإضافة إلى تحديد مخطط XML لملف المشروع |
| الخصائص والشروط | تتكون الخصائص من أزواج مفتاح - قيمة ويتم تعريفها ضمن عنصر PropertyGroup. يمثل اسم عنصر الخاصية مفتاح الخاصية ويحدد محتوى العنصر قيمة الخاصية
| العناصر و ItemGroups | العناصر الموجودة في ملف المشروع هي مدخلات لعملية الإنشاء مثل ملفات التعليمات البرمجية وملفات التكوين وملفات الأوامر وغيرها المطلوبة كجزء من عملية الإنشاء. العناصر ويجب تعريفها ضمن عنصر ItemGroup. |
| الأهداف والمهام | يمثل عنصر المهمة تعليمة (أو مهمة) بناء فردية. يتضمن MSBuild العديد من المهام المحددة مسبقًا مثل Copy و CSC و VBC و Exec. يجب أن يتم احتواء المهام دائمًا في عنصر `الهدف` وهو عبارة عن مجموعة من مهمة واحدة أو أكثر يتم تنفيذها بالتتابع ، ويمكن أن يحتوي ملف المشروع على أهداف متعددة.

## مراجع

* [Understanding the Project File](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [عناصر مخطط MSBuild](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference؟view=vs-2019)

