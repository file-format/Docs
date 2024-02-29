{
  "date": "2019-12-09",
  "keywords": [
"فایل zl",
"فرمت فایل zl",
"فایل zl چیست",
"فایل",
"مثال zl",
"پسوند فایل zl",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL - فرمت فایل فشرده ZLIP",
  "description": "با فرمت فایل ZL و APIهایی که می توانند فایل های ZL را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-fal"
}
},
  "lastmod": "2021-04-14"
}

## فایل ZL چیست؟

یک فایل با پسوند zl. یک فرمت فایل فشرده ZLIP است که از یک نوع الگوریتم فشرده سازی DEFLATE برای فشرده سازی فایل ها استفاده می کند. این مستقل از نوع CPU، سیستم عامل، سیستم فایل و مجموعه کاراکترها است و از این رو می تواند برای تبادل اطلاعات استفاده شود. مشخصات فنی فشرده سازی ZLIP در [IETF site](https://tools.ietf.org/html/rfc1950) موجود است و از دیدگاه توسعه دهنده قابل ارجاع است.

## فرمت فایل ZL

یک جریان zlib دارای ساختار زیر است:

 * CMF (روش فشرده سازی و پرچم ها) - این بایت بسته به روش فشرده سازی به یک روش فشرده سازی 4 بیتی و یک قسمت اطلاعاتی 4 بیتی تقسیم می شود.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * CM (روش فشرده سازی) - روش فشرده سازی مورد استفاده در فایل را مشخص می کند. مقادیر آن و روش فشرده سازی مربوطه به شرح زیر است.

| مقدار CM| فشرده سازی|
|---|---|
|CM = 8|DEFLATE با اندازه پنجره تا 32K|
|CM = 15|رزرو شده|

 * CINFO (اطلاعات فشرده سازی) - برای CM = 8، CINFO لگاریتم پایه 2 اندازه پنجره LZ77 است، منهای هشت (CINFO=7 اندازه پنجره 32K را نشان می دهد).

 * `FLG (FLaGs)` - این بایت پرچم به شرح زیر تقسیم می شود:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## منابع ##

* [مشخصات فرمت فایل Zlib](https://tools.ietf.org/html/rfc1950)


