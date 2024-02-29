{
  "date": "2020-08-20",
  "keywords": [
"فایل fon",
"فرمت فایل fon",
"فایل فون چیست",
"فایل",
"نمونه فون",
"پسوند فایل fon",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON - فایل کتابخانه فونت",
  "description": "با فرمت فایل FON و API هایی که می توانند فایل های FON را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-fan"
}
},
  "lastmod": "2020-10-30"
}

## فایل FON چیست؟

یک فایل با پسوند fon یک کتابخانه فونت مایکروسافت ویندوز 3.x است که در واقع یک فایل اجرایی است اما به fon. تغییر نام داده است. این مجموعه ای از فایل های [.fnt](/font/fnt/) به خودی خود است و برنامه ها هنگام دسترسی به فونت سیستم به آن ارجاع می دهند. به همین دلیل است که به عنوان یک فایل منبع عمل می کند. می توان آن را در سیستم عامل ویندوز با استفاده از برنامه Microsoft Windows Font View باز کرد.

## فرمت فایل FON

یک فایل FON حاوی منابع فونت است و فرمت فایل Resource (.res) دارد. فرمت فایل .res هدر فایل و همچنین مشخصات بخش داده را مشخص می کند. یک .fnt نیز یک فایل داده منبع است که همراه با یک فایل منبع است. فایل‌های FON دارای فرمت فایل باینری هستند و دارای نوع MIME برنامه‌ای/اکتت‌استریم هستند.

منابع فونت، بر خلاف انواع دیگر منابع، به منابع برنامه اضافه نمی شوند. در عوض به فایل‌های EXE اضافه می‌شوند و به فایل‌های fon. تغییر نام داده می‌شوند و در نتیجه به جای برنامه‌ها، فایل‌های کتابخانه‌ای ایجاد می‌شوند. فونت های متعدد فردی اجزای یک گروه فونت را تشکیل می دهند که در آن هر گروه از ساختار گروه منبع پیروی می کند. منابع فونت از این ساختارهای گروه منابع استفاده می کنند. هدر گروه دارای تمام اطلاعاتی است که برای دسترسی به یک فونت خاص از گروه مورد نیاز است. یک منبع جزء فونت فرمت زیر را دارد.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
یک فایل منبع .rc می‌تواند اعلان‌های منابع مختلط داشته باشد. گروه‌های فونت می‌توانند در هر جایی از فایل منبع باشند و لازم نیست به هم پیوسته باشند. برای برنامه‌هایی که فایل‌های RES را ایجاد می‌کنند باید وارد کردن دستی FONTDIR را اضافه کنند. در زیر ساختار هدر گروه آمده است.

```
[سرصفحه منبع عادی (نوع = 7)]

WORD NumberOfFonts; // تعداد کل در فایل RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
ساختار FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet؛
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily؛
WORD dfAvgWidth؛
WORD dfMaxWidth؛
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes؛
DWORD dfDevice;
DWORD dfFace؛
DWORD dfReserved.
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

