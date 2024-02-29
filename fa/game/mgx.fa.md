{
  "date": "2021-09-08",
  "keywords": [
"فایل mgx",
"فرمت فایل mgx",
"فایل mgx چیست؟",
"فایل",
"مثال mgx",
"پسوند فایل mgx",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل MGX Expansion Replay Age of Empires 2 و APIهایی که می‌توانند فایل‌های MGX ایجاد و باز کنند، بیاموزید.",
  "title": "MGX - Age of Empires 2 Expansion Replay",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mg-fax"
}
}،
  "lastmod": "2021-09-08"
}

## فایل MGX چیست؟

یک فایل با پسوند .mgx یک فایل ضبط شده برای بازی Age of Empires II: The Conquerors است که می تواند در برنامه Age of Empires II دوباره پخش شود. این شامل ضبط کامل کمپین بازی شده توسط کاربر است. می توان آن را در برنامه Age of Empires II بارگیری و پخش کرد. پس از پخش مجدد، بازی تمام رویدادها و سناریوهایی را که کاربر برای کمپین برنامه ریزی کرده و انجام داده را نشان می دهد.

## فرمت فایل MGX - اطلاعات بیشتر

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### تعاریف ساختار

اعتقاد بر این است که تعاریف ساختار فرمت فایل GPX بر اساس [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki) است که راهی برای خواندن و نوشتن داده‌های باینری ساخت یافته ارائه می‌کند. این به برنامه نویس اجازه می دهد تا فرمت داده های باینری را مشخص کند که سپس توسط BinData خوانده و می نویسد.

### پیام رسانی MGX

پیام رسانی MGX بر اساس دو نوع پیام است.

 * GAMESTART - دستورات شروع بازی را مشخص می کند و تا به امروز تأیید نشده است
 * CHAT - پیام های چت درون بازی را توصیف می کند. هم بازیکنان و هم خود بازی (Gaia) می توانند پیام های درون بازی منتشر کنند.

### اکشن های گیم پلی

چندین [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) وجود دارد که بازیابی شده‌اند و جزئیات آنها در دسترس است.

## منابع

* [عصر امپراتوری 2: فاتحان - مشخصات فرمت فایل Savegame] (https://github.com/stefan-kolb/aoc-mgx-format)


