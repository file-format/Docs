{
  "date": "2019-10-11",
  "keywords": [
"فایل tbz",
"فرمت فایل tbz",
"فایل tbz چیست",
"فایل",
"مثال tbz",
"پسوند فایل tbz",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "TBZ - بایگانی تار فشرده Bzip",
  "description": "درباره فرمت فایل TBZ و APIهایی که می‌توانند فایل‌های TBZ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tb-faz"
}
}،
  "lastmod": "2021-04-05"
}

## فایل TBZ چیست؟

یک فایل با پسوند tbz. یک آرشیو فشرده است که از فشرده سازی BZIP برای کاهش حجم فایل های محتوا استفاده می کند. فایل های TBZ در واقع فایل های آرشیو شده یونیکس [TAR](/compression/tar/) هستند که با BZIP فشرده می شوند. جدیدترین فشرده سازی سطح دوم [BZIP2](/compression/bz2/) است که جایگزین BZIP شد. فرمت فایل TBZ برای انتقال فایل های حجیم مناسب است. فایل های TBZ را می توان با استفاده از برنامه های نرم افزاری مانند 7-Zip، PeaZip و jZip باز یا استخراج کرد. کاربران لینوکس و macOS همچنین می توانند یک TBZ را با دستور BZIP2 از پنجره ترمینال باز کنند.

## فرمت فایل TBZ

فایل های TBZ در واقع آرشیوهای فشرده شده ای هستند که با فشرده سازی BZIP/[BZIP2](/compression/bz2/) ایجاد شده اند. هیچ مشخصات رسمی برای این فرمت فایل موجود نیست. با این حال، یک [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) غیر رسمی نشان می دهد که یک جریان .bz2 از یک سرصفحه 4 بایتی تشکیل شده است که با صفر یا بیشتر بلوک های فشرده دنبال می شود.

## منابع ##

* [مشخصات قالب BZIP2] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


