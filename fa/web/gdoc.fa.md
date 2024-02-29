{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل GDOC - میانبر Google Docs",
  "description": "درباره فایل GDOC و APIهایی که می‌توانند فایل‌های GDOC را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-fac"
}
},
  "lastmod": "2022-01-23"
}

## فایل GDOC چیست؟

فایل GDOC یک فایل میانبری است که به فایلی که در Google Drive، یک سرویس ذخیره‌سازی اسناد مبتنی بر ابر، قرار دارد، اشاره می‌کند. هنگامی که سرویس گیرنده Google Drive بر روی رایانه نصب می شود و سندی در داخل آن ایجاد می شود، درایو سندی را در فضای ذخیره سازی ابری آنلاین ایجاد می کند و [URL](/web/url/) این سند را در فایل GDOC در پوشه محلی Google Drive می نویسد. هنگامی که این فایل میانبر دوبار کلیک می شود، مرورگر وب پیش فرض سند را از مکان [URL](/web/url/) باز می کند. اگر این فایل میانبر به خارج از این پوشه منتقل شود، پیوند سند آنلاین خراب است.

## فرمت فایل GDOC - اطلاعات بیشتر

فایل GDOC حاوی میانبر برای سند آنلاین است که در قالب فایل [JSON](/web/json/) نوشته شده است. مرورگری که فایل‌های GDOC را باز می‌کند، اطلاعات URL را می‌خواند و سند پیوند داده شده را برای نمایش باز می‌کند، مشروط بر اینکه کاربر به این حساب Google که در آن سند ذخیره می‌شود وارد شده باشد. فایل‌های GDOC حاوی محتوای سند نیستند.

### مثال فایل GDOC

فایل GDOC را می توان در یک ویرایشگر متن باز کرد و محتوای آن مانند زیر است.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

همانطور که مشاهده می شود، محتویات به فرمت JSON دارای URL سند و شناسه سند مرتبط هستند.

## منابع

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

