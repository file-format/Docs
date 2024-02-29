{
  "date": "2020-01-11",
  "keywords": [
"فایل x",
"فرمت فایل x",
"فایل x چیست",
"فایل",
"x مثال",
"پسوند فایل x",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X - فرمت فایل DirectX 2.0",
  "description": "درباره فرمت فایل DirectX X و APIهایی که می توانند فایل های DirectX X را باز کرده و ایجاد کنند آشنا شوید.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--fax"
}
},
  "lastmod": "2020-01-11"
}

## فایل X چیست؟

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. برای رندر گرافیک سه بعدی در بازی ها استفاده می شد و ساختار مش ها، بافت ها، انیمیشن ها و اشیاء تعریف شده توسط کاربر را مشخص می کند. از سال 2014 منسوخ شده است زیرا فرمت فایل Autodesk FBX به عنوان یک فرمت مدرن تر عمل می کند. X قالب محور است و عاری از هرگونه دانش استفاده است.

می توانید فایل های DirectX X را با استفاده از Microsoft DirectX و ویرایشگرهای متن رایج باز کنید.

## فرمت فایل X

[X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) حاوی اطلاعات مرجع برای عناصر API است که برای کار با فایل‌های DirectX .x استفاده می‌شوند. این فرمت داده های اولیه سطح پایینی را ارائه می دهد که توسط سایر برنامه ها برای تعریف اولیه های سطح بالاتر از طریق قالب های داده استفاده می شود. DirectX 6.0 رابط ها و روش هایی را معرفی کرد که خواندن و نوشتن روی فایل های .x را امکان پذیر می کند. DirectX 3.0 نسخه باینری این فرمت فایل را معرفی کرد.

[X file format reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) تعریف شده توسط DirectX 9 حاوی اطلاعات مرجع برای فایل‌های x. در باینری و همچنین کدگذاری متن است.

### رمزگذاری باینری

[binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) فرمت DirectX X را به عنوان یک نمایش توکن شده از قالب متن تعریف می کند. این نشانه‌ها می‌توانند مستقل باشند تا ساختار دستوری بدهند یا می‌توانند توکن‌های رکورددار باشند که داده‌های لازم را فراهم می‌کنند.

#### سرتیتر

هدر باینری را می توان با استفاده از تعاریف زیر خواند و نوشت.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### کدگذاری متن

فایل های DirectX .x به نحوه استفاده از فایل بستگی ندارند و مختص هیچ برنامه ای نیستند. این رویکرد الگو محور اجازه می دهد تا فرمت فایل .x توسط هر برنامه مشتری استفاده شود.


#### سرتیتر

هدر با طول متغیر اجباری است و باید در ابتدای جریان داده باشد. هدر حاوی داده های زیر است.

|نوع |نوع فرعی |اندازه |مطالب |معنی محتوا|
---|---|---|---|---|
|شماره جادویی (الزامی)| | 4 بایت |xof |
|شماره نسخه (الزامی) |تعداد اصلی |2 بایت |03 |نسخه اصلی 3|
| |عدد مینور |2 بایت |02 |مینور نسخه 2|
|نوع قالب (الزامی)| |4 بایت |txt |پرونده متنی|
| | | |bin| فایل باینری|
| | | |tzip| فایل متنی فشرده MSZip|
| | | |bzip| فایل باینری فشرده MSZip|
|اندازه شناور (الزامی)| |4 بایت| 0064| شناورهای 64 بیتی|
| | | |0032 |شناورهای 32 بیتی|


## منابع

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [مرجع فرمت فایل DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

