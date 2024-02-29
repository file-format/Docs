{
  "date": "2022-04-01",
  "keywords": [
"فایل nkit",
"فرمت فایل nkit",
"فایل nkit چیست",
"فایل",
"نمونه nkit",
"پسوند فایل nkit",
"افزونه",
"قالب",
"فوتر nkit",
"فرمت فایل nkit"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل NKIT و APIهایی که می توانند فایل های NKIT را ایجاد و باز کنند آشنا شوید.",
  "title": "NKIT - فرمت فایل تصویر دیسک",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-fat"
}
}،
  "lastmod": "2022-04-01"
}

## فایل NKIT چیست؟

یک فایل NKIT یک تصویر دیسک از داده های استخراج شده از بازی های NintendoWii و GameCube است. NKIT برای قالب Nintendo Toolkit است. فایل فشرده سازی حاصل از [ISO](/compression/iso/) از داده های اصلی این بازی ها برای اجرا با برنامه های شبیه ساز مانند Dolphin، Swiss و Nintendon استفاده می کند. NKit در قالب‌های فایل خام (iso) و فشرده (gcz) عرضه می‌شود که هر دو با توجه به قابلیت پخش و اندازه طراحی شده‌اند.

## فرمت فایل NKIT

فرمت فایل NKit یک فرمت بدون ضرر است و برای کوچک کردن و بازیابی تصاویر Nintendo Wii و GameCube استفاده می شود. فرمت‌ها در فرمت‌های فایل ISO و GCZ برای هر یک از بازی‌های GameCube و Wii موجود هستند.

|سیستم | فرمت | پشتیبانی از سخت افزار | پشتیبانی از دلفین | قابل بازیابی 1:1 | یادداشت ها|
---|---|---|---|---|---|
|GameCube| nkit.iso| بله | بله| بله |همانند GameCube فشرده iso|
|GameCube| nkit.gcz| نه| بله| بله |GCZ فرمت فشرده سازی بلوک قابل جستجوی دلفین است|
| وای | nkit.iso| نه بله| بله| فرمت RVT-H فقط در Dolphin| قابل پخش است
| وای | nkit.gcz| نه بله| بله| RVT-H در GCZ فقط در Dolphin قابل پخش|

### سربرگ NKIT

هدر فرمت فایل NKIT به شرح زیر است.

|آفست |طول |نام|
---|---|---|
|0x200 |0x4 | سربرگ NKit 'NKIT'|
|0x204 |0x4 |نسخه NKit 'v01'|
|0x208 |0x4 |تصویر منبع اصلی CRC32|
|0x20C |0x4 |NKit CRC - باعث می شود فایل NKit CRC32 برابر با منبع CRC در 0x208 (در 0x4 در GCZ)|
|0x210 |0x4 |طول تصویر منبع|
|0x214 |0x4 |شناسه ناخواسته اجباری (وقتی شناسه دیسک متفاوت است - نادر - فقط GameCube)|
|0x218 |0x4 |Wii به روز رسانی پارتیشن CRC32 در صورت حذف در هنگام تبدیل|

## منابع ##

* [فرمت فایل NKIT - توسط gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


