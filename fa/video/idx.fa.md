{
  "date": "2022-07-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "IDX - کدک ویدیویی با کارایی بالا",
  "description": "درباره فرمت فایل IDX و APIهایی که می‌توانند فایل‌های IDX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "IDX",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-id-fax"
}
},
  "lastmod": "2022-07-12"
}

## فایل IDX چیست؟

یک فایل IDX یک فایل فهرست زیرنویس است که به لیست اطلاعات فراداده زیرنویس‌ها در یک فایل .sub (VobSub Subtitles) اشاره می‌کند. این برنامه توسط نرم افزار VobSub ایجاد و استفاده می شود که به کاربران امکان می دهد زیرنویس ها را از دی وی دی استخراج کرده و در یک فایل SUB قرار دهند. فایل‌های IDX حاوی مهرهای زمانی و بایت‌هایی هستند که برای اشاره به هر زیرنویس استفاده می‌شوند. VobSub همیشه یک فایل IDX همراه با فایل SUB مربوطه ایجاد می کند.

## فرمت فایل IDX - اطلاعات بیشتر

فایل های IDX به عنوان فایل های متنی ساده تولید و ذخیره می شوند که می توانند در هر ویرایشگر متنی باز شوند. یک فایل IDX حاوی اطلاعاتی است که توسط پخش کننده های رسانه برای خواندن پارامترهایی مانند رنگ متن زیرنویس برای نمایش روی صفحه، موقعیت متن زیرنویس روی صفحه خوانده می شود.

### تنظیمات زیرنویس IDX

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## نمونه فرمت فایل IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## چگونه از فایل IDX استفاده کنیم؟

اگر فایل‌های Sub و IDX را برای یک فیلم دارید، می‌توانید این زیرنویس‌ها را همراه با فیلمی که برای آن ساخته شده‌اند پخش کنید. بسیاری از برنامه ها مانند VLC، GOM Player، PotPlayer یا PowerDVD این قابلیت را دارند که این فایل های SUB و IDX را بارگذاری کنند و این فایل ها را در کنار فیلم پخش کنند. برنامه های نرم افزاری همچنین می توانند فایل های زیرنویس SUB و IDX را در فایل های [.mkv](/video/mkv/) جاسازی کنند.

## IDX را به SRT تبدیل کنید

[SRT](/video/srt/) (فرمت فایل SubRip) یک فایل زیرنویس ساده است که در قالب فایل SubRip ذخیره شده است. در مقایسه با فرمت فایل VobSub بیشتر مورد استفاده قرار می گیرد. بنابراین، اگر می‌خواهید فایل‌های SUB/IDX را به فرمت فایل SRT تبدیل کنید، ابزارهای شخص ثالثی در دسترس هستند که می‌توانند برای رسیدن به این هدف استفاده شوند. مبدل SUB/IDX به SRT، موجود در SubtitleTools.com یکی از ابزارهایی است که فایل های SUB و IDX را به عنوان ورودی می گیرد و این زیرنویس های VobSub را به فایل های SRT تبدیل می کند.

## منابع

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

