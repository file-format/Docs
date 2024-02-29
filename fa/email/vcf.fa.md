{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF - فایل تماس مجازی",
  "description": "درباره فرمت فایل VCF و API هایی که می توانند فایل های VCF ایجاد و باز کنند، بیاموزید.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-faf"
}
},
  "lastmod": "2019-09-10"
}

## فایل VCF چیست؟

VCF (فرمت کارت مجازی) یا کارت مجازی یک فرمت فایل دیجیتالی برای ذخیره اطلاعات تماس است. این قالب به طور گسترده برای تبادل داده در میان برنامه های کاربردی تبادل اطلاعات رایج استفاده می شود. اکثر سیستم عامل ها مانند ویندوز و MacOS دارای برنامه های پیش فرض برای ایجاد و باز کردن این فایل ها هستند. یک فایل VCF می تواند حاوی اطلاعات تماس برای یک یا چند مخاطب باشد. یک فایل VCF معمولا حاوی اطلاعاتی مانند نام مخاطب، آدرس، شماره تلفن، ایمیل، تولد، عکس ها و صدا علاوه بر تعدادی فیلد دیگر است. با پشتیبانی از سرویس گیرندگان و سرویس‌های ایمیل، در حین انتقال مخاطبین از طریق فرمت کارت مجازی، داده‌ای از دست نمی‌رود. نوع رسانه برای فرمت فایل VCF متن / کارت مجازی است.

## فرمت فایل VCF

فایل های VCF ذاتا متنی هستند و قابل خواندن توسط انسان هستند. اینها را می توان در ویرایشگرهای متنی مانند Notepad در Microsoft Windows و TextEdit در MacOS باز کرد. با این حال، اگر تصویری در فایل وجود داشته باشد، در ویرایشگر متن نمایش داده نمی شود.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) از باز کردن فایل‌های VCF و همچنین تبدیل به تعدادی فرمت دیگر مانند فرمت محبوب [MSG](/email/msg/) پشتیبانی می‌کند. فرمت فایل VCF با گذشت زمان از نسخه 2.1 تا 4.0 افزایش یافت و اطلاعات دقیقی را به فرمت فایل اضافه کرد. این قالب همچنین برای صادرات مخاطبین تلفن و سپس وارد کردن در دستگاه دیگری استفاده می شود.

{{< figure src="../VCF.png" alt="فرمت فایل VCF" >}}

### VCF 2.1 مثال

در زیر نمونه ای از نسخه 2.1 آورده شده است.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 مثال

در زیر نمونه ای از نسخه 3.0 آورده شده است.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 مثال

در زیر نمونه ای از نسخه 4.0 آورده شده است.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## منابع

* [VCF - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/VCard)


