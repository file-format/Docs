{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"فایل wpl",
"افزونه",
"قالب",
"فایل wpl چیست",
"موسیقی",
"فرمت فایل wpl"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل WPL و APIهایی که می‌توانند فایل‌های WPL را ایجاد، تبدیل و باز کنند، بیاموزید.",
  "title": "WPL - فایل لیست پخش Windows Media Player",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-fal"
}
},
  "lastmod": "2021-06-11"
}

## فایل WPL چیست؟

فایلی با پسوند wpl. حاوی لیست پخش آهنگ هایی است که باید در Microsoft Windows Media Player اجرا شوند. این فایل ها معمولا توسط کاربران برای مجموعه های ویدئویی و صوتی خود ایجاد می شوند. محتوای نوشته شده در یک فایل WPL، فقط مسیرهای دایرکتوری یا مکان هایی برای فایل های چندرسانه ای است که توسط سازنده فایل .wpl انتخاب شده است، بنابراین برنامه پخش کننده رسانه می تواند به سرعت محتوای چند رسانه ای را از محل دایرکتوری خود پیدا کرده و پخش کند.

## فرمت فایل WPL

WPL (Windows Media Player Playlist) یک فرمت فایل اختصاصی است که در Microsoft Windows Media Player نسخه 9 یا بالاتر استفاده می شود. این یک فرمت فایل کامپیوتری است که لیست های پخش چندرسانه ای را ذخیره می کند. به طور پیش‌فرض، فهرست پخش با پسوند .wpl (لیست پخش مدیا پلیر ویندوز) ذخیره می‌شود. اگر می‌خواهید دیسک‌های داده‌تان را در دستگاهی که از این افزونه پشتیبانی نمی‌کند پخش کنید، می‌توانید به جای آن از برنامه افزودنی [.m3u](/audio/m3u/) استفاده کنید. عناصر یک فایل WPL در قالب XML نشان داده شده است.

عنصر سطح بالا smil مشخص می کند که عناصر فایل از ساختار زبان ادغام چند رسانه ای همزمان (SMIL) پیروی می کنند. فایل با پسوند wpl ساخته و ذخیره می شود و نوع MIME آن application/vnd.ms-wpl است.

### مثال WPL

در اینجا نمونه ای از فایل wpl آورده شده است:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## منابع ##

* [MPEG-1 Audio Layer II - توسط Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


