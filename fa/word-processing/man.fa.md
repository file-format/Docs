{
  "date": "2021-07-25",
  "keywords": [
"مرد",
"فایل",
"افزونه",
"نوع",
"قالب",
"کتابچه راهنمای یونیکس"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "MAN - راهنمای یونیکس",
  "description": "درباره فرمت فایل FODT و APIهایی که می‌توانند فایل‌های MAN را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-fan"
}
}،
  "lastmod": "2021-07-25"
}

## فایل MAN چیست؟

یک فایل با پسوند man. مخفف man page است که یک کتابچه راهنمای کاربر برنامه نویسی یونیکس در قالب مستندات نرم افزاری است. این ابزار توسط ابزار Man موجود در یونیکس استفاده می شود که برای مشاهده اسناد استفاده می شود. اسناد نرم افزار حاوی اطلاعاتی در بخش ها و صفحات است که با استفاده از ابزار Man از ترمینال فرمان با صدور دستورات قابل بازیابی هستند. از آنجایی که در رایانه به عنوان نسخه نرم افزاری اسناد موجود است، برای دسترسی به آن نیازی به نسخه چاپی یا اتصال اینترنتی نیست.

## فرمت فایل Man Manual Unix - اطلاعات بیشتر

صفحات Man در قالب متن ساده ذخیره می شوند و می توانند در هر ویرایشگر متنی برای مشاهده یا ویرایش ایجاد و باز شوند. در یونیکس، اطلاعات صفحات Man با صدور دستوراتی از ترمینال که شامل ارجاع به بخش و شماره صفحه از دفترچه راهنما است، بازیابی می شود.

### بخش ها و صفحات

Unix man راهنمای سیستم است که در آن هر آرگومان صفحه به فرمان به نام یک برنامه، ابزار یا تابع اشاره دارد. دستور، در صورت ارائه اطلاعات بخش، صفحه را در آن بخش خاص جستجو می کند. با این حال، رفتار پیش فرض این است که صفحه را در همه بخش ها جستجو کنید و صفحه اول را صرف نظر از اینکه در چندین بخش وجود داشته باشد، نمایش دهید.

### شماره بخش

در زیر اطلاعاتی در مورد شماره بخش های دفترچه راهنما به همراه انواع صفحات آنها ارائه شده است.

|شماره بخش|نوع صفحات|
---|---|
|1|برنامه های اجرایی یا دستورات پوسته|
|2| فراخوانی های سیستم (توابع ارائه شده توسط هسته)|
|3| فراخوانی های کتابخانه (عملکرد در کتابخانه های برنامه)|
|4|فایل های ویژه (معمولاً در /dev یافت می شوند)|
|5|فرمت ها و قراردادهای فایل، به عنوان مثال /etc/passwd|
|6|بازی|
|7|متفرقه (شامل بسته ها و قراردادهای کلان)، به عنوان مثال man(7)، groff(7)|
|8|دستورات مدیریت سیستم (معمولاً فقط برای روت)|
|9|روالهای هسته [غیر استاندارد]|

## مثال - چگونه صفحات MAN را بخوانیم؟

در اینجا مثالی از نحوه بازیابی اطلاعات در مورد دستور MkDir با استفاده از دستور Man آورده شده است.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## منابع

* [مشخصات فنی OpenDocument - توسط ویکی پدیا](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) - صفحه راهنمای لینوکس](https://man7.org/linux/man-pages/man1/man.1.html)


