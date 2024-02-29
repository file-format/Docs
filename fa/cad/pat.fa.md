{
  "date": "2020-03-16",
  "keywords": [
"فایل PAT",
"قالب",
"CAD"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل PAT و APIهایی که می‌توانند فایل‌های PAT را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل PAT",
  "linktitle": "PAT",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-pa-fat"
}
}،
  "lastmod": "2020-10-25"
}

## فایل PAT چیست؟

یک فایل با پسوند pat یک فایل CAD است که توسط نرم افزار اتوکد استفاده می شود. برنامه‌هایی که می‌توانند فایل‌های PAT را باز کنند، از الگوی دریچه ذخیره‌شده در این فایل‌ها استفاده می‌کنند، اطلاعاتی در مورد بافت/پرکردن یک ناحیه دریافت می‌کنند. الگوهای موجود اطلاعاتی در مورد ظاهر مواد به اشیاء ترسیم شده می دهد. فایل های PAT را می توان در برنامه هایی مانند Autodesk AutoCAD، CorelDRAW Graphics Suite و Ketron Software باز کرد. فایل های PAT را می توان به فرمت های تصویری مختلف مانند JPG، PNG، BMP و غیره تبدیل کرد.

## فرمت فایل PAT

فایل های PAT در قالب متن ساده نوشته می شوند و می توانند در هر ویرایشگر متنی باز شوند. الگوهای دریچه ای در این فایل ها مبتنی بر برداری هستند و از نحو مشخص شده توسط مستندات اتوکد پیروی می کنند.

همه الگوها از نقطه 0.0 شروع می شوند، الگو برای پوشش مرز جوجه کشی محاسبه می شود.

### تعریف الگو

تمام تعاریف الگو شامل فیلدهای زیر است:
 * یک '\*' پیشرو
 * یک نام - نام نمی تواند فاقد فاصله، علائم نگارشی، پرانتز یا اسلید باشد.
 * A description

The standard format for hatch patterns is `<\*><name><, description>`. The name and the description are separated by a comma and descriptions cannot exceed the eighty character line length. The hatch patterns are defined after this information.

### نمونه های الگوی دریچه
در زیر نمونه ای از الگوی مربع آورده شده است
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
مثال دیگری که الگوی متوازی الاضلاع را نشان می دهد به شرح زیر است.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## منابع ##

 * [Hash Patterns by Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

