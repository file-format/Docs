{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
}،
  "draft" : "false",
  "toc" : true,
  "description":"درباره فرمت فایل OSR و APIهایی که می‌توانند فایل‌های OSR را ایجاد و باز کنند، بیاموزید.",
  "title" : "فایل OSR - osu! بازپخش فرمت فایل",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-fa",
      "parent" : "game"
}
}،
  "lastmod" : "2021-09-08"
}

## فایل OSR چیست؟

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**MIME نوع فرمت فایل OSR:** x-osu-replay

## فرمت فایل OSR

فایل های OSR به صورت فایل های باینری با فیلدهای داده با طول ثابت و متغیر ذخیره می شوند.

|نوع داده| قالب|
---|---|
|بایت |حالت بازی بازپخش (0 = osu! استاندارد، 1 = تایکو، 2 = ضرب و شتم، 3 = osu!mania)|
|عدد صحیح |نسخه بازی زمانی که پخش مجدد ایجاد شد (مثلا 20131216)|
|رشته |osu! بیت مپ MD5 هش|
| رشته | نام بازیکن|
| رشته | اوسو! پخش مجدد هش MD5 (شامل ویژگی های خاصی از پخش مجدد)|
|کوتاه| تعداد 300s|
|کوتاه| تعداد 100 در استاندارد، 150 در تایکو، 100 در CTB، 100 در مانیا|
|کوتاه| تعداد 50 در استاندارد، میوه ریز در CTB، 50 در شیدایی|
|کوتاه| تعداد Geki در استاندارد، حداکثر 300s در شیدایی|
|کوتاه| تعداد Katus در استاندارد، 200s در Mania|
|کوتاه| تعداد از دست دادن|
|عدد صحیح| مجموع امتیاز نمایش داده شده در گزارش امتیاز|
|کوتاه| بهترین ترکیب نمایش داده شده در گزارش امتیاز|
|بایت| ترکیبی عالی/کامل (1 = بدون از دست دادن و بدون شکستن نوار لغزنده و بدون لغزنده تمام شده زود هنگام)|
|عدد صحیح| مدهای استفاده شده برای لیست مقادیر mod به زیر مراجعه کنید.|
| رشته | نمودار نوار زندگی: جفت‌های u/v جدا شده با کاما، که در آن u زمان ورود به آهنگ بر حسب میلی‌ثانیه است و v یک مقدار ممیز شناور از 0 - 1 است که نشان‌دهنده میزان عمر شما در زمان معین است (0 = نوار عمر: خالی، 1= نوار زندگی پر است)|
|طولانی| تمبر زمان (تیک ویندوز)|
|عدد صحیح| طول بر حسب بایت داده های بازپخش فشرده|
|بایت |آرایه داده های بازپخش فشرده|
|طولانی| شناسه امتیاز آنلاین|
|دوبل| اطلاعات مود اضافی فقط در صورتی ارائه شود که Target Practice فعال باشد.|

## منابع

* [OSU! بازی ریتم](https://osu.ppy.sh/home)

* [فرمت فایل OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


