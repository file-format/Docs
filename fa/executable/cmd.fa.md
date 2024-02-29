{
  "date": "2021-07-12",
  "keywords": [
"فایل cmd",
"فایل cmd چیست",
"فایل",
"نمونه cmd",
"پسوند فایل cmd",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل CMD و APIهایی که می توانند فایل های CMD را ایجاد و باز کنند، بیاموزید.",
  "title": "CMD - فرمت فایل فرمان ویندوز",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-fad"
}
},
  "lastmod": "2021-07-12"
}

## فایل CMD چیست؟
یک فایل CMD شامل یک اسکریپت حاوی یک یا چند دستور به شکل متن ساده است که به منظور اجرای وظایف مختلف اجرا می شوند. این شبیه به یک فایل [BAT](/executable/bat/) است که معمولاً برای ذخیره مجموعه ای از دستورات اجرایی نیز استفاده می شود. فایل های CMD به طور گسترده در سیستم عامل مایکروسافت ویندوز استفاده می شود. این فایل ها تقریباً در دهه 90 معرفی شدند اما هنوز در آخرین سیستم عامل ویندوز استفاده می شوند. این فایل ها معمولا برای اجرای بیش از یک دستور در یک دنباله نوشته می شوند.

## فرمت فایل CMD
CMD یک فرمت فایل است که توسط برنامه های اجرایی به سبک CP/M استفاده می شود. به طور کلی با [COM](/executable/com/) در CP/M-80 و [EXE](/executable/exe/) در DOS قابل مقایسه است. یک فایل CMD شامل 1 تا 8 گروه کد یا داده و هدر 128 بایتی است. اندازه هر گروه می تواند تا 1 مگابایت باشد. فایل‌های CMD همچنین می‌توانند حاوی اطلاعات جابجایی و پسوندهای سیستم مقیم (RSX) در نسخه‌های بعدی آن باشند. CMD در مقایسه با فایل [BAT](/executable/bat/) تازه وارد است. برای MS-DOS قبل از انتشار ویندوز در MS-DOS استفاده می شود. اگرچه امروزه هنوز هم می‌توانید فایل‌ها را با پسوند bat ذخیره کنید، بسیاری از افراد از پسوند cmd. برای ذخیره اسکریپت‌های اجرایی خود استفاده می‌کنند.

### مشخصات فرمت CMD

شروع هدر شامل لیستی از گروه های موجود در فایل به همراه انواع آنها می باشد. هر نوع را می توان حداکثر یک بار استفاده کرد. این انواع عبارتند از:

- کد
- داده ها
- اضافی
- پشته
- کاربر 1
- کاربر 2
- کاربر 3
- کاربر 4
- کد مشترک

به همین ترتیب، پیشوند بخش برنامه در DOS، 256 بایت اول گروه داده صفر است. آنها با CP/M-86 با صفحه صفر پر می شوند. اگر گروه داده ای وجود نداشته باشد، به جای آن از 256 بایت اول گروه کد استفاده می شود.
## نمونه فایل CMD
در زیر نمونه ای از اسکریپت CMD برای نمایش اطلاعات سیستم ها آورده شده است.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## منابع 

* [چگونه یک اسکریپت CMD بنویسیم](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [فایل CMD (CP/M) - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


