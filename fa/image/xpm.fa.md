{
  "date": "2019-10-11",
  "keywords": [
"فایل xpm",
"فرمت فایل xpm",
"فایل xpm چیست",
"فایل",
"مثال xpm",
"پسوند فایل xpm",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPM - فرمت فایل X PixMap",
  "description": "درباره فرمت فایل XPM و APIهایی که می‌توانند فایل‌های XPM را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XPM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-xp-fam"
}
},
  "lastmod": "2019-09-10"
}

## فایل XPM چیست؟

یک فایل با پسوند xpm. یک فرمت فایل تصویری است که توسط سیستم X Windows استفاده می‌شود. از پیکسل‌های شفاف پشتیبانی می‌کند و معمولاً نقشه‌های پیکسلی را ایجاد می‌کند. از داده های تک رنگ، gra-scale و pixmap رنگی پشتیبانی می کند. اینها به گونه ای طراحی شده اند که با دست قابل ویرایش هستند و می توانند در کد [C](/programming/c/) گنجانده شوند. برای این منظور فایل های XPM در قالب فایل متنی ساده هستند و از سینتکس زبان برنامه نویسی C پیروی می کنند. فایل های XPM را می توان با انواع برنامه های مشاهده تصویر مانند
CorelDRAW Graphics Suite 2020، Corel PaintShop Pro، IrfanView و Canvas X.

## فرمت فایل XPM

فرمت فایل XPM از سینتکس C استفاده می کند تا در برنامه های C و C++ یکپارچه شود. از شش بخش مختلف زیر تشکیل شده است.

 * \<Values>
 * \<Colors>
 * \<Pixels>
 * \<Extensions>

بخش ها در واقع آرایه ای از رشته ها به شرح زیر هستند.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
در ادامه جزئیات هر بخش آورده شده است.

`<Values> ` - این بخش یک رشته است که شامل چهار یا شش عدد صحیح است که در پایه 10 قرار دارند و مطابق با:

 * عرض و ارتفاع pixmap
 * تعداد رنگ
 * تعداد کاراکتر در هر پیکسل
 * مختصات هات اسپات اختیاری و تگ XPMEXT

`<Colors> ` - این بخش به تعداد رنگ ها رشته دارد. هر رشته به صورت زیر است:

```
<chars>{<key><color> }+
```
`<Pixels> ` - این بخش تشکیل شده است<height> رشته ها و<width> \*<chars_per_pixel> شخصیت ها. هر<chars_per_pixel> رشته طول باید یکی از گروه های تعریف شده قبلی در باشد<Colors> بخش.

`<Extension> ` - بخش پسوند باید در صورت خالی نبودن برچسب گذاری شود<Values> بخش. ممکن است از چندین تشکیل شده باشد<Extension> بخش های فرعی که ممکن است از دو نوع زیر باشند:

 * یک رشته مستقل به صورت زیر تشکیل شده است: XPMEXT<extension-name><extension-data>
 * یا بلوکی که توسط چندین رشته تشکیل شده است: XPMEXT<extension-name><related extension-data composed of several strings>

## منابع

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)

* [راهنمای XPM] (http://www.xfree86.org/current/xpm.pdf)


