{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"درباره فایل .pak و APIهایی که می‌توانند فایل‌های PAK را ایجاد و باز کنند، بیاموزید.",
  "title" : "فرمت فایل PAK- فایل بسته بازی ویدیویی",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-fa",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## فایل PAK چیست؟

فایل PAK یک فایل بسته است که توسط بازی های ویدیویی مختلف برای آرشیو داده های بازی ایجاد می شود. در اصل، این یک فرمت فایل بازی است. این می تواند شامل چندین عنصر بازی مانند گرافیک، بافت، صداها، اشیاء و سایر داده های بازی باشد. آرشیو بیشتر به صورت فایل .zip ذخیره می شود و می توان آن را با نرم افزارهای رفع فشرده سازی محبوب مانند WinZip و WinRAR استخراج کرد. نمونه هایی از بازی های ویدیویی با استفاده از فایل های PAK شامل Quake، Hexen، Crysis و Half-Life هستند.

## فرمت فایل PAK - اطلاعات بیشتر

در بیشتر موارد، فایل‌های PAK در [ZIP file format](/compression/zip/) ذخیره می‌شوند. اما برنامه های مختلف ممکن است از فرمت های مختلف فایل برای ذخیره این فایل ها استفاده کنند.


## چگونه فایل های PAK را باز کنیم؟

می‌توانید فایل‌های PAK را با برنامه‌هایی مانند [PakExplorer](https://www.quaketerminus.com/tools.shtml) و [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) باز کنید.

**---------------------------------------------- ------------------------------------------------ -----------------------**

## فرمت فایل PAK - فایل شیء Simutrans

فایلی با پسوند .pak فرمت فایل بازی شبیه سازی حمل و نقل [Simutrans](https://www.simutrans.com/en/) است. این شامل اشیاء مورد استفاده در شبیه سازی مانند گرافیک ساخته شده توسط کاربر و محتویات داده است. این می تواند چندین شی مختلف مانند وسایل نقلیه بازی، ساختمان ها، زمین و غیره داشته باشد. فایل های PAK با استفاده از MakeObject، ابزاری که فایل های .dat و تصاویر png. را برای ایجاد این اشیاء شبیه سازی کامپایل می کند، تولید می شوند. Simutrans به بازیکنان اجازه می دهد تا با ساخت و مدیریت سیستم های حمل و نقل مسافران، پست و کالا از طریق زمین، یک سیستم حمل و نقل موفق را اجرا کنند.

## چگونه فایل های PAK ایجاد کنیم؟

Simutrans نمونه هایی را برای ایجاد فایل های PAK در سیستم عامل ویندوز و لینوکس فهرست کرده است.

### سیستم عامل ویندوز

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### لینوکس BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## منابع

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

