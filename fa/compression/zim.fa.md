{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل ZIM - فایل بایگانی OpenZIM",
  "description": "با فرمت فایل ZIM و APIهایی که می توانند فایل های ZIM را ایجاد و باز کنند آشنا شوید.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-fam"
}
}،
  "lastmod": "2019-12-09"
}

## فایل ZIM چیست؟ ##

فایل‌های با پسوند zim. آرشیوهایی هستند که برای ذخیره محتوای ویکی آفلاین ایجاد شده‌اند. این به عنوان مناسب ترین فرمت فایل باز برای ذخیره ویکی پدیا بر روی USB در نظر گرفته می شود. محتویات سایت را در قالب فشرده ذخیره می کند. نام آن از Zeno IMproved که فرمت اولیه فایل Zeno بود گرفته شده است. ZIM توسط پروژه [openZIM ](https://openzim.org/) که توسط ویکی‌مدیا CH حمایت می‌شود و توسط بنیاد ویکی‌مدیا پشتیبانی می‌شود، نگهداری می‌شود. فایل های ZIM را می توان با برنامه هایی مانند Kiwix و ZIMReader باز کرد. پروژه OpenZIM اجرای فرمت فایل ZIM را در [Github](https://github.com/openzim) برای مشارکت انجمن OpenSource میزبانی کرده است.

## مشخصات فرمت فایل ZIM

قالب فایل ZIM در بالای [Zeno file format](https://openzim.org/wiki/Zeno_file_format) ایجاد شده است و با عقب سازگار نیست. مشخصات فرمت فرمت فایل ZIM [available online](https://openzim.org/wiki/ZIM_file_format) توسط openZIM برای مرجع توسعه دهنده می باشد. OpenZIM اجرای متن باز C++، [LibZim](https://openzim.org/wiki/Zimlib) را برای خواندن و نوشتن فایل های ZIM ارائه کرده است.

فرمت فایل ZIM از فشرده سازی LZMA2 برای فشرده سازی محتوا استفاده می کند.

{{< figure src="../ZIM_File_Format.jpeg" alt="فرمت فایل ZIM" >}}


### سربرگ ZIM

A ZIM file starts with a header that is at offset 0. همه اجزای سازنده بر اساس little-endian هستند و همه اعداد صحیح اعداد صحیح بدون علامت هستند یعنی uint_16، uint_32، uint_64.

|نام فیلد |نوع| افست| طول| توضیحات|
---|---|---|---|---|
|MagicNumber| عدد صحیح| 0| 4| عدد جادویی برای تشخیص فرمت فایل باید 72173914 (0x44D495A) باشد|
|نسخه اصلی| عدد صحیح| 4| 2| نسخه اصلی فرمت فایل ZIM (5 یا 6)|
|minorVersion| عدد صحیح| 6| 2| نسخه کوچک فرمت فایل ZIM|
|uuid| عدد صحیح| 8| 16| شناسه منحصر به فرد این فایل zim|
|ArticleCount| عدد صحیح| 24| 4| تعداد کل مقالات|
|clusterCount| عدد صحیح| 28| 4| تعداد کل خوشه ها|
|urlPtrPos| عدد صحیح| 32| 8| موقعیت فهرست اشاره گر دایرکتوری مرتب شده بر اساس URL|
|titlePtrPos| عدد صحیح| 40| 8| موقعیت فهرست اشاره گر دایرکتوری مرتب شده بر اساس عنوان|
|clusterPtrPos| عدد صحیح| 48| 8| موقعیت فهرست نشانگر خوشه|
|mimeListPos| عدد صحیح| 56| 8| موقعیت لیست نوع MIME (همچنین اندازه سرصفحه)|
|صفحه اصلی| عدد صحیح| 64| 4| صفحه اصلی یا 0xffffffff اگر صفحه اصلی وجود ندارد|
|layoutPage| عدد صحیح| 68| 4| صفحه layout یا 0xffffffffff در صورت عدم وجود صفحه طرح|
|checksumPos| عدد صحیح| 72| 8| اشاره گر به md5checksum این فایل بدون خود چک sum. این همیشه 16 بایت قبل از پایان فایل نشان می دهد.|

## منابع ##

* [OpenZIM](https://openzim.org/)

* [C++ LibZim] (https://openzim.org/wiki/Zimlib)


