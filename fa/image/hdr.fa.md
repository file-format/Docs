{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل HDR - فایل تصویری HDR چیست؟",
  "description": "درباره فرمت فایل HDR و APIهایی که می‌توانند فایل‌های HDR را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-far"
}
}،
  "lastmod": "2022-07-21"
}

## فایل HDR چیست؟

فایل HDR یک فرمت تصویر شطرنجی با محدوده دینامیکی بالا (HDR) برای ذخیره عکس‌های دوربین دیجیتال است. این امکان را به ویرایشگرهای عکس می دهد تا رنگ و روشنایی تصاویر دیجیتالی را که محدوده دینامیکی محدودی دارند، افزایش دهند. این اصلاح می تواند روشنایی اطراف گوشه ها را بهبود بخشد و در نتیجه تصویری نزدیک به طبیعی ایجاد کند. فایل های HDR معمولاً به صورت تصاویر شطرنجی 32 بیتی ذخیره می شوند. Adobe Photoshop می تواند فایل های HDR ایجاد و باز کند.

فایل های HDR با نام HDRI نیز شناخته می شوند.

## فرمت فایل HDR - اطلاعات بیشتر

فرمت فایل HDR بر اساس فرمت اصلی فایل Radiance Picture (pic.) است. داده‌های پیکسلی یک فایل HDR معمولاً به صورت فشرده ذخیره نمی‌شوند، اما در برخی موارد با استفاده از یک سیستم رمزگذاری طول اجرا مستقیم فشرده می‌شوند.

### ساختار فایل HDR

یک فایل تصویری HDR از سه بخش زیر تشکیل شده است:

 * **سرصفحه:** یک فایل HDR با اولین بایت های فایل تصویر یعنی #?RADIANCE شناسایی می شود.
 * **رشته رزولوشن:** سرصفحه با یک خط وضوح منفرد دنبال می شود که از 4 مقدار تشکیل شده است. یک برچسب X و Y که هر کدام با یک عدد صحیح عددی همراه است. ترتیب X و Y نشان دهنده چرخش است. ترکیب X و Y با مقادیر مثبت و منفی تمام جهت گیری ها و چرخش های ممکن iamge را پوشش می دهد.
 * **Pixel Data:** داده های پیکسلی یک فایل HDR یا فشرده نشده یا با استفاده از یک رمزگذاری استاندارد طول اجرا فشرده می شود.

## APIهای منبع باز HDR/HDRI

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - کتابخانه تک سرصفحه [C++](/programming/cpp/) با پلتفرم متقاطع برای دریافت اندازه و قالب تصویر بدون بارگیری/رمزگشایی.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - کتابخانه زنگ زده برای دریافت اندازه و قالب تصویر بدون بارگیری/رمزگشایی. [.avif](/image/avif/)، [.bmp](/image/bmp/)، [.cur](/image/cur/)، [.dds](/image/dds/)، [. .gif](/image/gif/)، hdr (pic)، [heic (heif)](/image/heic/)، [.icns](/image/icns/)، [.ico](/image/ ico/)، [.jp2](/image/jp2/)، [jpeg (jpg)](/image/jpeg/)، [jpx](/image/jpx/)، ktx، [png](/image/ png/)، [psd](/image/psd/)، qoi، tga، tiff (tif)، و webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - اجرای جاوا HdrHistogram.

## منابع

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

