{
  "date" : "2021-06-29",
  "keywords" :["DLL" , "الامتداد" , "الملف" , "التنسيق" , "النظام" , "مكتبة الارتباط الديناميكي" , "الإعدادات" , "البرامج" , "الكمبيوتر" , "التطبيق"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - مكتبة الارتباط الديناميكي" ,
  "description":"تعرف على تنسيق ملف DLL وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DLL وفتحها." ,
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-06-29"
}

## ما هو ملف DLL؟ ##

يعد ملف DLL أو مكتبة الارتباط الديناميكي نوعًا من الملفات القابلة للتنفيذ. إنه أحد أكثر ملفات الامتداد شيوعًا على جهازك ويتم تخزينه عادةً في مجلد System32 على نظام Windows الخاص بك. تم تطوير ملف ملحق DLL بواسطة Microsoft ويستخدم بشكل شائع من قبلهم. لديها شعبية عالية تصنيف المستخدم. يعمل DLL كرف يحتوي على * برامج التشغيل / الإجراءات / الوظائف / الخصائص * التي تم تصميمها وتطبيقها على برنامج / تطبيق بواسطة خادم Windows. يمكن أيضًا مشاركة ملف DLL واحد بين برامج windows المختلفة. تعد ملفات الامتداد هذه ضرورية للتشغيل السلس لبرامج Windows على جهازك لأنها مسؤولة عن تمكين وتشغيل العديد من الوظائف على البرنامج مثل كتابة وقراءة الملفات والاتصال بأجهزة أخرى خارجية لإعدادك.
ومع ذلك ، لا يمكن فتح هذه الملفات إلا على جهاز يدعم أي إصدار من Windows (windows 7 / windows 10 / etc.) وبالتالي لا يمكن فتحها مباشرة على جهاز يدعم نظام التشغيل Mac OS. (إذا كنت تريد فتح ملف DLL على نظام التشغيل Mac OS ، فيمكن أن تساعد التطبيقات الخارجية المختلفة في فتحها.)


## تنسيق ملف DLL ##

تم تطوير ملف DLL بواسطة Microsoft ولديه الامتداد ".dll" الذي يمثل النوع. لقد كان جزءًا لا يتجزأ من خادم Windows 1.0 وما بعده. إنه نوع ملف ثنائي وتدعمه جميع إصدارات Microsoft Windows. تم إنشاء هذا النوع من الملفات كوسيلة لإنشاء نظام مكتبة مشترك ضمن برامج Windows ، للسماح بإجراء تعديلات أو تغييرات منفصلة ومستقلة في مكتبات البرامج دون الحاجة إلى إعادة ربط البرامج.


## مثال DLL ##

يمكن العثور على رمز مثال لنقطة إدخال DLL أدناه:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## المرجعي ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
