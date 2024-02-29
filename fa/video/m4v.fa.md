{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"فایل",
"افزونه",
"قالب",
"MPEG-4",
"مدیریت حقوق دیجیتال",
"DRM",
"سیب",
"ویدئو"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "درباره فرمت فایل M4V و APIهایی که می‌توانند فایل‌های M4V را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-fav"
}
},
  "lastmod": "2019-09-14"
}

## فایل M4V چیست؟

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V از H.264 برای ویدیو و **[AAC](/audio/aac/)** و Dolby Digital برای رمزگذاری و رمزگشایی صدا استفاده می‌کند.

## ساختار فایل M4V ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V با نوع فرعی که باید M4V_ باشد تعریف شده است. نوع تکه‌های دیگر امضاهای از پیش تعریف‌شده هستند: ftyp، mdat، moov، pnot، udta، uuid، moof، رایگان، پرش، jP2، wide , load، ctab، imap، matt، kmat، clip، crgn، sync، chap، tmcd، scpt، ssrc،  تصویر. با تکرار تکه ها، تا زمانی که نوع ناشناخته شناسایی شود، فایل M4V را می سازیم.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. در آفست 32 (هگز: 20) قطعه دوم قرار دارد که اندازه آن 30322 است (هگزا: 00 00 76 72، big-endian، ابتدا بایت پایین) و نوع **moov** (هگز: 6D 6F 6F است. 76). قطعه بعدی در افست 32+30322#30354 (هگز: 00 00 76 92) قرار دارد و دارای اندازه 8 (هگز: 00 00 00 08) و نوع **رایگان** (هگز: 66 72 65 65) است.
### کدک های مورد استفاده در M4V ###

#### Video Codec H.264 ####

H.264 یک استاندارد فشرده‌سازی ویدئو است که ویدئوهای دیجیتال را به فرمتی تبدیل می‌کند که در صورت نیاز به انتقال یا ذخیره‌سازی، فضای کمتری نیاز دارد. M4V از H.264 برای فشرده سازی ویدئو استفاده می کند. کاربرد آن از DVD، تلویزیون، ویدئو کنفرانس و پخش ویدئو از طریق اینترنت می باشد. H.264 از دو بخش اصلی تشکیل شده است: رمزگذار – که ویدیو را فشرده می کند، رمزگشا – که ویدیوی فشرده شده را از حالت فشرده خارج می کند. در شکل زیر فرآیندهای کدگذاری و رمزگشایی مشخص شده اند و سایر فرآیندها در استاندارد H.264 پوشش داده شده اند.

##### فرآیند کدگذاری و رمزگشایی ویدئو در H.264 #####

برای جریان بیت فشرده H.264، رمزگذار ویدئو فرآیند پیش‌بینی، تبدیل و رمزگذاری را انجام می‌دهد. در همان زمان، رمزگشا فرآیند معکوس رمزگشایی، تبدیل معکوس و بازسازی را برای تولید مجدد فایل ویدئویی انجام می دهد. اندازه H.264 نصف MPEG است.

#### کدک صوتی ####

Advanced Audio Coding (AAC) یک کدک صوتی برای فشرده سازی صدای دیجیتال با اتلاف است و در ظرف M4V استفاده می شود. AAC جانشین فرمت [MP3](/audio/mp3/) است و کیفیت بهتری نسبت به MP3 با همان میزان بیت دارد. فرمت AAC برخی از اطلاعات را در طول فرآیند فشرده سازی دور می اندازد که از اهمیت کمتری برخوردار است. AAC یک کدک مبتنی بر بلوک با نرخ بیت متغیر (VBR) است که در آن هر بلوک به 1024 نمونه دامنه زمانی رمزگشایی می‌شود.

### منابع ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)

* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


