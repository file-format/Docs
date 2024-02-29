{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"فایل usdz",
"فرمت فایل usdz",
"فرمت فایل",
"3 بعدی",
"دانلود فایل usdz"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ - فرمت ZIP توضیحات صحنه جهانی",
  "description": "درباره فرمت فایل USDZ و APIهایی که می‌توانند فایل‌های USDZ را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-faz"
}
},
  "lastmod": "2021-02-01"
}

## فایل USDZ چیست؟

یک فایل با .usdz یک آرشیو ZIP فشرده نشده و رمزگذاری نشده برای فرمت فایل [USD](/3d/usd/) (شرح جهانی صحنه) است که حاوی و پروکسی برای فایل‌های فرمت‌های دیگر (مانند بافت‌ها و انیمیشن‌ها) تعبیه‌شده در بایگانی است و آنها را اجرا می‌کند. مستقیماً با زمان اجرا USD بدون نیاز به باز کردن بسته بندی. فایل‌های USDZ بسته‌هایی هستند که طراحی آن‌ها بر اساس انتزاع سطح Ar جدید یک بسته است. Usdz در IANA ثبت شده است و دارای نام نوع رسانه مدل و نام زیرشاخه vnd.usd+zip است و جزئیات آن را می‌توانید در [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip) پیدا کنید.

## فرمت فایل USDZ

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### محدودیت ZIP

فرمت فایل USDZ از فرمت فایل ZIP بدون «فشرده سازی» و «رمزگذاری» استفاده می کند. هدف این طراحی برای برآوردن دو الزام بود:

 * برای بسته‌ای که قبلاً در حافظه بارگذاری شده است یا به‌عنوان یک فایل واحد روی دیسک، API به USD برای دسترسی به داده‌های موجود در تصویر موجود است.
 * نیازی به استخراج فایل ها روی دیسک یا تخصیص فضای ذخیره سازی بیشتر وجود ندارد

با USDZ، هر دوی این الزامات برآورده می‌شوند، زیرا اکثر فرمت‌های تصویری خود، طرح‌های فشرده‌سازی داخلی را امکان‌پذیر می‌کنند که در نتیجه اندازه فایل فشرده می‌شود.

### الزامات چیدمان

بسته‌های USDZ به چیدمان فایل‌های درون بسته نیاز دارند به این صورت که داده‌های هر فایل باید در مضربی از ۶۴ بایت از ابتدای بسته شروع شود. با این حال، در صورت هدف قرار دادن بسته با یک مرجع ساده، بسته باید با یک فایل بومی [USD](/3d/usd/) شروع شود. در چنین حالتی، این اولین فایل USD به عنوان لایه پیش فرض نامیده می شود. مشتریانی که مایل به ارائه محتوای قابل جریان هستند ممکن است بخواهند سایر محدودیت های طرح بندی را نیز در نظر بگیرند.

## دانلود فایل USDZ
از آنجایی که فایل‌های usdz مملو از تصاویر با کیفیت بالا و فایل‌های usd هستند، می‌توانند فضای ذخیره‌سازی دیسک بیشتری را اشغال کنند. در اینجا می توانید یک فایل مثال ساده و کوچکتر USDZ را برای دانلود پیدا کنید:

- [Sample.usdz](../sample.usdz)

## منابع

* [مشخصات فرمت فایل USDZ](https://openusd.org/release/spec_usdz.html)


