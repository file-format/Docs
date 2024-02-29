{
  "date": "2023-05-16",
  "keywords": [
"فایل سامی",
"فایل سامی چیست",
"نمونه فایل سامی",
"فایل",
"پسوند فایل sami",
"افزونه"
]،
  "author": {
    "display_name": "Shakeel Faiz"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل SAMI - زیرنویس و فایل تبادل ابرداده",
  "description": "درباره فرمت SAMI و APIهایی که می‌توانند فایل‌های SAMI را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-fa",
      "parent": "video"
}
}،
  "lastmod": "2023-05-16"
}

## فایل SAMI چیست؟

یک فایل با پسوند .sami معمولا به یک فایل زیرنویس و تبادل ابرداده (SAMI) اشاره دارد. SAMI یک قالب زیرنویس است که برای نمایش زیرنویس یا زیرنویس در ویدیوها استفاده می شود. در ابتدا توسط مایکروسافت برای Windows Media Player توسعه داده شد.

فایل‌های SAMI حاوی اطلاعات زمان‌بندی و محتوای متنی برای زیرنویس‌ها یا زیرنویس‌ها هستند که به آنها امکان می‌دهد با پخش ویدیو همگام شوند. این قالب از گزینه های قالب بندی اولیه مانند سبک قلم، رنگ و موقعیت زیرنویس ها بر روی صفحه پشتیبانی می کند.

فایل های SAMI معمولاً فایل های متنی ساده هستند و می توان آنها را با استفاده از یک ویرایشگر متن باز و ویرایش کرد. محتویات یک فایل SAMI معمولاً شامل یک بخش سرصفحه است که اطلاعات مربوط به فایل را ارائه می‌کند و به دنبال آن ورودی‌های زیرنویس جداگانه با زمان و متن مربوطه خود را ارائه می‌دهد.

در اینجا مثالی از شکل ظاهری یک فایل SAMI آمده است:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

فایل‌های SAMI معمولاً همراه با پخش‌کننده‌های ویدیو یا پخش‌کننده‌های رسانه‌ای که از نمایش زیرنویس پشتیبانی می‌کنند، مانند Windows Media Player یا VLC Media Player استفاده می‌شوند. پخش‌کننده فایل SAMI را می‌خواند و زیرنویس‌ها را با محتوای ویدیو همگام‌سازی می‌کند و به بینندگان اجازه می‌دهد هنگام تماشای ویدیو، زیرنویس‌ها را بخوانند.

## تگ های HTML پشتیبانی شده

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` عنصر ریشه که کل فایل SAMI را کپسوله می کند.
- ``<HEAD> :`` حاوی اطلاعات سرصفحه فایل SAMI است.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` ویژگی های فونت را برای متن محصور شده تعریف می کند. برای تغییر ظاهر فونت می توان از ویژگی هایی مانند رنگ، چهره، اندازه و سبک استفاده کرد.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` متن محصور شده را به صورت پررنگ نمایش می دهد.</b>
- `` <I>:`` متن محصور شده را به صورت مورب ارائه می کند.</i>
- `` <U>:`` متن ضمیمه شده را با زیرخط نمایش می دهد.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

اینها برخی از تگ های اساسی هستند که توسط فایل های SAMI پشتیبانی می شوند. توجه به این نکته مهم است که SAMI طیف کاملی از برچسب‌ها و ویژگی‌های HTML را پشتیبانی نمی‌کند. تگ های پشتیبانی شده در درجه اول بر روی استایل و قرار دادن زیرنویس ها متمرکز هستند تا ساختاردهی یا تعامل گسترده سند.

## منابع
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


