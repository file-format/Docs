{
  "date" : "2021-02-20",
  "keywords" :["WMA" , "ملف" , "امتداد" , "تنسيق" , "تنسيق ملف تبادل الصوت" , "موسيقى"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف WMA وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات WMA وفتحها." ,
  "title" :"WMA - ملف صوتي لـ Windows Media" ,
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
} ,
  "lastmod" : "2021-02-20"
}

## ما هو ملف WMA؟

يمثل الملف بامتداد .wma ملفًا صوتيًا يتم حفظه بتنسيق الأنظمة المتقدمة (ASF). ASF هو تنسيق مملوك لشركة Microsoft ويحتوي على دفق بتات مشفر بواسطة Windows Media Audio 9. بالإضافة إلى محتوى الصوت ، يحتوي ملف WMA أيضًا على كائنات بيانات وصفية مثل العنوان والألبوم والفنان ونوع المسار. تُستخدم ملفات WMA بشكل أساسي للدفق عبر الويب على غرار ملفات [.mp3](/ar/audio/mp3/).

## تنسيق ملف WMA

ملف WMA هو تنسيق ملف ثنائي ويتم تضمينه في تنسيق ملف ASF. يحدد ترميز البيانات الوصفية حول الملف على غرار علامات ID3 المستخدمة بواسطة ملفات MP3. تستخدم Microsoft برنامج ترميز WMA في تنسيق الملف المحمي القابل للتشغيل البيني (PIFF) منذ عام 2008. ومع ذلك ، لم يتم الإعلان عنه كبرنامج ترميز صوتي قياسي من خلال معايير الصناعة ذات الصلة مثل DECE UltraViolet و MPEG-DASH.

### البيانات الخاصة بنوع WMA

يتم تخزين المعلومات الخاصة بالنوع لبرنامج ترميز Windows Media Audio بالتنسيق التالي كجزء من البيانات الخاصة بالنوع لكائن خصائص الدفق.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## مراجع

* [نظرة عامة على ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

