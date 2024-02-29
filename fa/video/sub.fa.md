{
  "date": "2023-06-21",
  "keywords": [
"فایل فرعی",
"فایل فرعی چیست",
"نمونه ای از فایل زیرنویس MicroDVD",
"پسوندهای زیرنویس",
"زیر را باز کنید",
"انواع فایل زیرنویس",
"نحوه باز کردن فایل SUB",
"فایل",
"پسوند فایل SUB",
"افزونه"
]،
  "author": {
    "display_name": "Shakeel Faiz"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل SUB - فایل زیرنویس MicroDVD",
  "description": "درباره قالب SUB و APIهایی که می توانند فایل های SUB ایجاد و باز کنند، بیاموزید.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub-fa",
      "parent": "video"
}
}،
  "lastmod": "2023-06-21"
}

## فایل SUB چیست؟

فایل SUB یک فرمت فایل زیرنویس MicroDVD است که برای نمایش زیرنویس‌ها در ویدیوها استفاده می‌شود که معمولاً دارای پسوند فایل .sub هستند. این فایل ها حاوی اطلاعات زمان بندی و متن برای هر ورودی زیرنویس هستند.

فایل‌های زیرنویس MicroDVD از فرمت ساده مبتنی بر متن استفاده می‌کنند که هر ورودی زیرنویس از چندین خط تشکیل شده است. خط اول حاوی اطلاعات زمان بندی زیرنویس، از جمله مهرهای زمانی شروع و پایان است. خطوط بعدی حاوی متن زیرنویس واقعی است.

Here is an example of MicroDVD subtitle file:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## پسوندهای زیرنویس

Subtitles can have various file extensions depending on format they are in. Some common subtitle file extensions include:

- **.srt:** SubRip subtitle format. It is one of most widely used subtitle formats and is supported by many media players and video editing software.
- **.sub:** Subtitle file format that can be used by different subtitle formats, such as MicroDVD, SubViewer and SubStation Alpha.
- **.ass or .ssa:** Advanced SubStation Alpha or SubStation Alpha subtitle format. It supports advanced features like text formatting, positioning and effects.
- **.vtt:** WebVTT (Web Video Text Tracks) format used for displaying subtitles on web videos. It is commonly used with HTML5 video players.
- **.idx/.sub:** Format used by DVD subtitles. The .idx file contains timing and formatting information, while .sub file contains the actual subtitle text.
- **.smi or .sami:** Synchronized Accessible Media Interchange format. It is commonly used for closed captions and subtitles in Windows Media Player.

## منظور از Open Sub چیست؟

Open Sub معمولاً به معنای OpenSubtitles است که یک پلتفرم آنلاین محبوب است که زیرنویس فیلم ها و برنامه های تلویزیونی را به چندین زبان ارائه می دهد. این مجموعه گسترده ای از فایل های زیرنویس ارائه شده توسط جامعه کاربران خود را ارائه می دهد. برای جستجو و دانلود زیرنویس فیلم ها یا سریال های تلویزیونی مورد نظر خود می توانید به وب سایت OpenSubtitles (www.opensubtitles.org) مراجعه کنید.

## انواع فایل زیرنویس

Subtitle files come in various formats, each with its own file type or extension. Here are some common subtitle file types:

- **SubRip Subtitle Format (.srt):** This is one of most widely used subtitle formats. SRT files are plain text files that contain subtitle entries with timestamps and corresponding text.
- **SubViewer Subtitle Format (.sub):** SubViewer files are similar to SRT files, contain subtitle entries with timestamps and text, may support additional features such as text formatting and colors.
- **SubStation Alpha (.ssa) and Advanced SubStation Alpha (.ass):** These formats support advanced features like text formatting, styling, positioning and animation effects. SSA and ASS files are commonly used for anime subtitles.
- **MicroDVD Subtitle Format (.sub):** MicroDVD format uses .sub files and includes timing information and text for each subtitle entry. It is often used with media players and video editing software.
- **DVD Subtitles (.sub and .idx):** DVD subtitles typically consist of two files: the .sub file, which contains subtitle text, and .idx file, which contains timing and formatting information.
- **WebVTT (.vtt):** WebVTT is a subtitle format used for web videos, commonly used with HTML5 video players and supports basic formatting options.
- **MPL2 Subtitle Format (.mpl):** MPL2 files are used with MPlayer, a media player for Unix-like systems, contain subtitle entries with timestamps and text.
- **iTunes Timed Text (.itt):** iTunes Timed Text files are used for subtitles in Apple's iTunes and other Apple platforms. They support features like text styling and positioning.
- **Teletext Subtitle Format (.srt or .txt):** Teletext subtitles are commonly used in broadcast television. They are usually saved as plain text files with .srt or .txt extensions.

## چگونه فایل SUB را باز کنیم؟

پخش‌کننده‌های رسانه زیر می‌توانند فایل SUB را به عنوان آهنگ زیرنویس باز کنند.

- پخش کننده رسانه VideoLAN VLC
- MPlayer

برای باز کردن فایل SUB در پخش کننده VLC این مراحل را دنبال کنید

- پخش کننده VLC را باز کنید و ویدیوی خود را پخش کنید
- از نوار منوی VLC Media Player، **Subtitles > Add Subtitle File ....** را انتخاب کنید.
- به فایل SUB بروید و آن را باز کنید

اگر نیاز به ویرایش فایل SUB دارید، می توانید آن را با هر ویرایشگر متنی مانند Microsoft Notepad (ویندوز) یا Apple TextEdit (Mac) باز کنید.

## منابع
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)


