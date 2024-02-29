{
  "date": "2021-06-09",
  "keywords": [
"نشانه",
"فایل",
"افزونه",
"قالب",
"فایل نشانه چیست",
"موسیقی",
"فرمت فایل نشانه",
"مشخصات فرمت فایل cue",
"برگه نشانه",
"CDRWIN"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل CUE و APIهایی که می‌توانند فایل‌های CUE را ایجاد، تبدیل و باز کنند، بیاموزید.",
  "title": "CUE - فایل ورق نشانه",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-fae"
}
}،
  "lastmod": "2021-07-01"
}

## فایل CUE چیست؟

یک فایل با پسوند cue. که به عنوان فایل برگه نشانه نیز شناخته می‌شود، یک فایل فراداده است که حاوی اطلاعاتی در مورد طرح‌بندی آهنگ‌ها بر روی CD یا DVD است. این ها توسط پخش کننده های رسانه و برنامه های نوشتن دیسک نوری پشتیبانی می شوند. داده‌های صوتی اصلی ذخیره‌شده روی سی‌دی توسط فایل نشانه، همراه با مشخصات طول آهنگ، عنوان دیسک و اجراکنندگان ارجاع می‌شوند. بنابراین اگر یک فایل صوتی شامل چندین تراک باشد، می توان از فایل نشانه برای تقسیم صدا به چندین فایل یا ارجاع به تراک های مختلف استفاده کرد.

## فرمت فایل CUE

فایل‌های CUE یا صفحه نشانه در قالب متن ساده که برای انسان قابل خواندن است ذخیره می‌شوند. اطلاعات موجود در یک فایل نشانه دستوراتی با یک یا چند پارامتر هستند. بسته به دستور خاص و زمینه، این دستورات یا بر روی کل فایل اعمال می شود یا برای یک آهنگ جداگانه. راهنمای کاربر CDRWIN مشخصات نحو و معنای صفحه نشانه را شرح می دهد.

## دستورات اساسی برگه CUE

|فرمان|توضیحات|
---|---|
|فایل| به فایل حاوی داده ها و قالب آن مانند [MP3](/audio/mp3/)، [WAV](/audio/wav/) یا تصویر دیسک باینری ساده)|
| آهنگ| اطلاعات زمینه آهنگ مانند تعداد و نوع یا حالت آن را تعریف می کند.|
|INDEX| موقعیت را به عنوان یک شاخص در داخل FILE نشان می دهد. فرمت mm:ss:ff (دقیقه-ثانیه فریم) است.|
|PREGAP و POSTGAP|این نشان دهنده پیش شکاف یا پس شکاف یک آهنگ است که در هیچ فایل داده ای ذخیره نمی شود. طول در همان قالب دقیقه-ثانیه فریم برای INDEX مشخص شده است.|

### مثال ورق CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## سایر فایل های CUE

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.cue** استفاده می کنند.

**دیسک و رسانه**
- [CUE - فایل ورق نشانه](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## منابع

* [فایل cda - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/.cda_file)


