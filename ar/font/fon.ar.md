{
  "date" : "2020-08-20",
  "keywords" :["fon file", "fon file format", "what is a fon file", "file", "fon example", "fon file extension", "extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"FON - ملف مكتبة الخطوط" ,
  "description":"تعرف على تنسيق ملف FON وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات FON وفتحها." ,
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
} ,
  "lastmod" : "2020-10-30"
}

## ما هو ملف FON؟

الملف ذو الامتداد .fon هو مكتبة خطوط Microsoft Windows 3.x وهي في الواقع ملف قابل للتنفيذ ولكن تمت إعادة تسميته إلى .fon. وهي عبارة عن مجموعة من ملفات [.fnt](/ar/font/fnt/) في حد ذاتها وتشير التطبيقات إليها أثناء الوصول إلى خط النظام. هذا هو السبب في أنها تعمل كملف موارد. يمكن فتحه على نظام تشغيل Windows باستخدام تطبيق Microsoft Windows Font View.

## تنسيق ملف FON

يحتوي ملف FON على موارد الخط وله تنسيق ملف Resource (.res). يحدد تنسيق ملف .res عنوان الملف بالإضافة إلى مواصفات قسم البيانات. .fnt هو أيضًا ملف بيانات مورد مضمن مع ملف مورد. تحتوي ملفات FON على تنسيق ملف ثنائي ولديها تطبيق / ثماني دفق نوع MIME.

لا تتم إضافة موارد الخطوط ، بخلاف الأنواع الأخرى من الموارد ، إلى موارد التطبيق. وبدلاً من ذلك يتم إضافتها إلى ملفات EXE وإعادة تسميتها إلى ملفات .fon ، مما ينتج عنه ملفات مكتبة بدلاً من التطبيقات. تشكل الخطوط الفردية المتعددة مكونات مجموعة الخطوط حيث تتبع كل مجموعة بنية مجموعة موارد. تستخدم موارد الخطوط هياكل مجموعة الموارد هذه. يحتوي عنوان المجموعة على جميع المعلومات المطلوبة للوصول إلى خط معين من المجموعة. مورد مكون الخط له التنسيق التالي.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/ar/font/fnt/) file)
```
يمكن أن يحتوي ملف مورد .rc واحد على تعريفات موارد مختلطة. يمكن أن تكون مجموعات الخطوط في أي مكان في ملف المورد ويجب ألا تكون متجاورة. يجب أن تضيف البرامج التي تنشئ ملفات .RES الإدخال اليدوي لـ FONTDIR. فيما يلي هيكل رأس المجموعة.

""
[رأس مورد عادي (النوع = 7)]

كلمة NumberOfFonts ؛ // العدد الإجمالي في ملف .RES
```     
The remaining data is repeated for every font in the .RES file.

```
كلمة الخط
struct FontDirEntry {
كلمة dfVersion ؛
DWORD dfSize ؛
شار dfCopyright [60] ؛
كلمة dfType ؛
WORD dfPoints ؛
كلمة dfVertRes ؛
كلمة dfHorizRes ؛
كلمة dfAscent ؛
كلمة dfInternalLeading ؛
كلمة dfExternalLeading ؛
BYTE dfItalic؛
BYTE dfUnderline ؛
BYTE dfStrikeOut ؛
كلمة df الوزن.
BYTE dfCharSet ؛
كلمة dfPixWidth ؛
كلمة dfPixHeight ؛
BYTE dfPitchAndFamily ؛
كلمة dfAvgWidth ؛
كلمة dfMaxWidth ؛
BYTE dfFirstChar ؛
BYTE dfLastChar ؛
BYTE dfDefaultChar ؛
BYTE dfBreakChar ؛
كلمة dfWidthBytes ؛
DWORD dfDevice ؛
DWORD dfFace ؛
تم حجز DWORD df ؛
char szDeviceName [] ،
char szFaceName [] ؛
} ؛
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

