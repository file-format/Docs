{
  "date": "2021-02-15",
  "keywords": [
"فایل vp6",
"فرمت فایل vp6",
"فایل vp6 چیست",
"فایل",
"نمونه vp6",
"پسوند فایل vp6",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "VP6 - فایل ویدئویی TrueMotion",
  "description": "درباره فرمت فایل VP6 و APIهایی که می‌توانند فایل‌های VP6 را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-fa6"
}
}،
  "lastmod": "2021-02-16"
}

## فایل VP6 چیست؟

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. این بخشی از سری کدک های ویدئویی است که توسط TrueMotion شامل V3، V4 و V5 توسعه یافته است. این فرمت در مدت کوتاهی در زمینه پخش مانند گزارش های BBC و نرم افزار QuickLink مورد استفاده قرار گرفت. VP6 توسط VP7 Codec در ژانویه 2005 با سازگاری فشرده سازی بهتر جایگزین شد.

## فرمت فایل VP6

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### ماکروبلاک (MB)

مشابه MPEG-2، MPEG-4 قسمت های 2 و 10، هر فریم ویدیویی از یک فایل VP6 از آرایه ای از ماکروبلاک های 16x16 (MB) تشکیل شده است. هر مگابایت می تواند در یکی از حالت های زیر باشد:

 * داخل مگابایت
 * Inter MB، null MV، مرجع فریم قبلی
 * Inter MB، دیفرانسیل MV، مرجع فریم قبلی
 * Inter MB، چهار MV، مرجع فریم قبلی
 * Inter MB، MV 1، مرجع فریم قبلی
 * Inter MB، MV 2، مرجع فریم قبلی
 * اینتر مگابایت، MV تهی، مرجع فریم نشانک شده
 * Inter MB، دیفرانسیل MV، مرجع فریم نشانه گذاری شده
 * Inter MB، MV 1، مرجع قاب نشانه گذاری شده
 * Inter MB، MV 2، مرجع قاب نشانه گذاری شده

### هدر فریم

هدر فریم یک VP6 مطابق شکل زیر است که از بسته بندی بیت بیگ اندیان پیروی می کند.

|Syntax|تعداد بیت|نوع|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 به معنای درون فریم| است
|qp |6 |بدون علامت | پارامتر کوانتیزاسیون محدوده معتبر 0..63|
| نشانگر| 1| ثابت| 0=VP61/62، 1=VP60|
|if (حالت_فریم == 0) { | 0 | |برابر با INTRA_FRAME|
|نسخه |5| ثابت| 6=VP60/61، 7=VP60(Electronic Arts)، 8=VP62|
|نسخه2 |2| ثابت |0=VP60، 3=VP61/62|
|رابط |1| Boolean |true (1) به این معنی است که از interlace استفاده خواهد شد|
|if (نشانگر==1 یا نسخه2==0) {||||
|افست |16 |بدون امضا| افست بافر ثانویه (بایت های مربوط به شروع بافر)|
|}||||
| dim_y |8| بدون امضا| ارتفاع ماکروبلاک ویدیو|
|dim_x |8| بدون امضا| عرض ماکروبلاک ویدیو|
|render_y |8 |بدون امضا |ارتفاع نمایش ویدیو|
|render_x |8 |بدون علامت |عرض نمایش ویدیو|
|}دیگر{||||
|if (نشانگر==1 یا نسخه2==0) {||||
|offset |16 |بدون علامت | افست بافر ثانویه (بایت های مربوط به شروع بافر)|
|}||||
|}||||

## منابع

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


