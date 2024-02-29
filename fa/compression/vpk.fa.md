{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فایل VPK - فرمت فایل بسته برنامه پلی استیشن ویتا",
  "description": "با فرمت فایل VPK و API هایی که می توانند فایل های VPK ایجاد و باز کنند آشنا شوید.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-fak"
}
}،
  "lastmod": "2022-03-01"
}

## فایل VPK چیست؟

یک فایل با پسوند vpk. یک فایل بسته آرشیو فشرده است که برای نصب برنامه های شخص ثالث روی کنسول بازی Sony PlayStation Vita استفاده می شود. این فایل‌ها را می‌توان تنها بر روی جیلبریک ویتا پلی‌استیشن توسط HENkaku نصب کرد که PS Vita و PSTV را قادر می‌سازد تا از محتوای سفارشی‌سازی شده کاربر استفاده کنند. یک فایل بایگانی VPK حاوی تمام محتویاتی است که بازی را می‌سازد، از جمله تصاویری مانند فایل‌های [PNG](/image/png/)، فایل‌های تنظیمی مانند [.bin](/disc-and-media/bin/)، و هر گونه پیکربندی در قالب فایل [XML](/web/xml/).

## فرمت فایل VPK

فایل‌های VPK به عنوان آرشیوهای فشرده استاندارد [ZIP](/compression/zip/) روی دیسک ذخیره می‌شوند. اینها ممکن است حاوی چندین پوشه و سایر فایل‌های مرتبط برای برنامه‌های شخص ثالث برای نصب در کنسول بازی ویتا باشند. برای مشاهده محتویات فایل بسته VPK، پسوند آن را از .vpu به .zip تغییر نام دهید، و محتویات را با استفاده از ابزارهای استاندارد رفع فشرده سازی مانند WinZip یا WinRAR استخراج کنید.

نرم افزار Valve اطلاعات دقیقی در مورد [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format) دارد که می توان از دیدگاه توسعه دهنده به آنها اشاره کرد.

## چگونه فایل های VPK را نصب کنیم؟

فایل های VPK را می توان از ابزار خط فرمان VPK.exe نصب کرد. در سیستم عامل ویندوز، فایل ها را می توان در فایل vpk.exe رها کرد که یک \*.vpk حاوی تمام فایل های بسته بندی شده را برمی گرداند. همچنین می‌توان از ابزار خط فرمان به صورت زیر استفاده کرد.

### VPK ایجاد کنید و فایل ها را اضافه کنید

```
vpk <dirname>
```

### فایل های VPK را استخراج کنید

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## نمایشگر VPK

 * [VRF VPK Viewer] (https://github.com/SteamDatabase/ValveResourceFormat)

## منابع

* [فرمت فایل VPK] (https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [فایل های VPK] (https://developer.valvesoftware.com/wiki/VPK)


