{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل MKV",
  "keywords": [
"mkv",
"ویدیوی matroska",
"فرمت mkv",
"نحوه پخش فایل های mkv",
"ویدئو",
"فایل",
"قالب"
]،
  "description": "درباره فرمت فایل MKV و APIهایی که می‌توانند فایل‌های MKV را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-fav"
}
}،
  "lastmod": "2020-17-11"
}


## فایل MKV چیست؟ ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- پشتیبانی از جستجوی سریع
- امکان انتخاب جریان های مختلف صوتی و تصویری.
- پشتیبانی از زیرنویس ها (کد سخت و نرم کد).
- پشتیبانی از ابرداده ها، فصل ها و منوها.
- قابلیت پخش آنلاین
- امکان بازیابی فایل های اشتباهی که قابلیت پخش فایل های خراب را فراهم می کند.

## تاریخچه مختصر ##

فایل MKV در سال 2002 در روسیه ایجاد شد. توسعه دهنده اصلی Lasse Kärkkäinen بود که با بنیانگذار Matroska، Steve Lhomme، و تیمی از برنامه نویسان کار می کرد. MKV به عنوان یک پروژه استانداردهای باز توسعه یافته است، به این معنی که منبع باز و رایگان برای استفاده است. با گذشت زمان، این فرمت بهبود یافت و اساس فرمت چند رسانه ای WebM در سال 2010 شد.

## طراحی ماتروسکا ##

Matroska محدودیت های زیر را به مشخصات EBML اضافه می کند.

- **EBML Header** **docType** باید 'matroska' باشد.
- **EBML Header** **EBMLMaxIDLength** باید 4 باشد.
- **EBMLMaxSizeLength***EBML Header** باید بین 1 تا 8 (شامل) باشد.

تمام عناصر سطح بالا در 4 اکتت کدگذاری شده اند.

- کدهای زبان: Matroska (نسخه 1 تا 3) از کدهای زبانی استفاده می‌کند که می‌توانند از فرم 3 حرفی ISO-639-2 کتابشناختی (مانند fre برای فرانسوی) یا کد کشور اضافی مانند fre-ca استفاده شوند. برای فرانسوی کانادایی. با شروع در Matroska نسخه 4، ممکن است از ISO 639-2 یا BCP 47 برای کدهای زبان استفاده شود، اگرچه BCP 47 توصیه می شود.
- انواع فیزیکی: این ها هم برای فایل های صوتی و هم برای فایل های تصویری معنای متفاوتی دارند. برای مثال ChapterPhysicalEquiv = 60 به معنی (CD / 12 اینچ / 10 اینچ / 7 اینچ / TAPE / MINIDISC / DAT) برای صدا و (DVD / VHS / LASERDISC) برای ویدیو است.
- ساختار بلوک - سربرگ بلوک: هدر بلوک حاوی اطلاعاتی در مورد شماره آهنگ، مهرهای زمانی، نوع بند و غیره است.
- Lacing: مکانیزمی برای صرفه جویی در فضا در هنگام ذخیره سازی داده ها است که معمولاً برای بلوک های کوچک داده (فریم) استفاده می شود. 3 نوع توری وجود دارد:
  - "Xiph: قاب با مضرب اندازه 255 با کد 0 در انتهای اندازه. به عنوان مثال، کد 765 255;255;255;0 است."
  - "EBML: اندازه فریم به عنوان تفاوت بین اندازه قبلی و این اندازه کدگذاری می شود. اندازه اول توری بدون علامت است، اما دیگران از تغییر دامنه برای دریافت علامت روی هر مقدار استفاده می کنند."
  - "fixed-size: اندازه ثابت باقی می ماند."
- ساختار SimpleBlock: از ساختار **بلاک** الهام گرفته شده است که تفاوت اصلی آن اضافه شدن پرچم های **Keyframe** و **Discardable** است. غیر از این، همه چیز یکسان است.

## ساختار ماتروسکا ##

یک سند Matroska باید حداقل از یک **EBML Document** با استفاده از **Matroska Document Type** تشکیل شده باشد. هر **EBML Document** باید با یک **EBML Header** و سپس **EBML Root Element** شروع شود که به عنوان یک بخش تعریف می شود. Matroska چندین عنصر سطح بالا را تعریف می کند که ممکن است در قسمت **Segment** رخ دهد.

EBML از یک سیستم عناصر برای نوشتن یک سند EBML استفاده می کند، لیست زیر لیست عناصر سطح بالا در فایل Matroska است:

- **EBML Document**: Wrapper برای کل فایل.
- **EBML Header**: حاوی اطلاعات هدر فایل مانند DocType است.
- **Segment**: عنصر بالایی که شامل سایر عناصر سطح بالا می باشد.
- **SeekHead**: شامل موقعیت بخش های دیگر عناصر سطح بالا می باشد.
- **اطلاعات**: حاوی اطلاعات کلی در مورد بخش است.
- **تراک**: یک عنصر سطح بالا از اطلاعات با تعداد زیادی آهنگ توصیف شده است.
- **Chapters**: It is used to define basic menus and partition data.
- **خوشه**: عنصر سطح بالا حاوی ساختار Block.
- **Cues**: یک عنصر سطح بالا که شامل تمام ورودی های محلی به بخش است که دسترسی به جستجو را سرعت می بخشد.
- **ضمیمه ها**: این شامل فایل های پیوست می باشد.
- **برچسب ها**: این عنصر حاوی ابرداده است که آهنگ ها، نسخه ها، فصل ها، پیوست ها یا بخش را به طور کلی توصیف می کند.

جدول زیر ساختار سند Matroska را با اکثر عناصر نمایش داده شده در یک سلسله مراتب نشان می دهد:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| سربرگ EBML | | | |
| بخش | SeekHead| جستجو | شناسه جستجو |
| | | | SeekPosition |
| | اطلاعات | SegmentUID | |
| | | SegmentFilename | |
| | | PrevUID | |
| | | نام فایل قبلی | |
| | | NextUID | |
| | | نام فایل بعدی | |
| | | بخش خانواده | |
| | | فصل ترجمه | |
| | | TimestampScale | |
| | | مدت زمان | |
| | | DateUTC | |
| | | عنوان | |
| | | MuxingApp | |
| | | WritingApp | |
| | آهنگ | TrackEntry | شماره آهنگ |
| | | | TrackUID |
| | | | TrackType |
| | | | نام |
| | | | زبان |
| | | | CodecID |
| | | | CodecPrivate |
| | | | کدکنام |
| | | | ویدیو | FlagInterlaced |
| | | | | Field Order |
| | | | | حالت استریو |
| | | | | حالت آلفا |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | عرض نمایش |
| | | | | ارتفاع صفحه نمایش |
| | | | | Aspect RatioType |
| | | | | رنگ |
| | | | صوتی | SamplingFrequency |
| | | | | کانال ها |
| | | | | BitDepth |
| | فصل ها | Edition Entry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | فصل اتم | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapterFlagHidden |
| | | | | ChapterDisplay | ChapString |
| | | | | | ChapLanguage |
| | خوشه | مهر زمان |
| | | SilentTracks |
| | | موقعیت |
| | | اندازه قبلی |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | نشانه ها | CuePoint | CueTime |
| | | | CueTrackPositions |
| | پیوست ها | فایل پیوست | توضیحات فایل |
| | | | نام فایل |
| | | | FileMimeType |
| | | | FileUID |
| | | | ارجاع فایل |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | برچسب ها | برچسب | اهداف | TargetTypeValue |
| | | | | نوع هدف |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | برچسب ساده | نام برچسب |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | برچسب باینری |
| | | | | SimpleTag |


### استفاده از کدک ها ###

اگر یک پخش کننده رسانه جدید نمی خواهید و ترجیح می دهید از پخش کننده موجود خود استفاده کنید، باید چند کدک (مخفف فشرده سازی/فشرده سازی) نصب کنید. حتی اگر دانلود کدک ها گزینه معتبری است، باید مراقب منبع باشید و ممکن است حاوی بدافزار باشند.

## منابع ##

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

