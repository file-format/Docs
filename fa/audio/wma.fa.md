{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"فایل",
"افزونه",
"قالب",
"فرمت فایل تبادل صدا",
"موسیقی"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل WMA و APIهایی که می‌توانند فایل‌های WMA را ایجاد و باز کنند، بیاموزید.",
  "title": "WMA - فایل صوتی Windows Media",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-faa"
}
},
  "lastmod": "2021-02-20"
}

## فایل WMA چیست؟

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. علاوه بر محتوای صوتی، یک فایل WMA همچنین حاوی اشیاء فراداده مانند عنوان، آلبوم، هنرمند و سبک آهنگ است. فایل‌های WMA عمدتاً برای پخش جریانی روی وب مشابه فایل‌های [.mp3](/audio/mp3/) استفاده می‌شوند.

## فرمت فایل WMA

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. با این حال، توسط استانداردهای صنعتی مرتبط مانند DECE UltraViolet و MPEG-DASH به عنوان کدک صوتی استاندارد اعلام نشده است.

### WMA Type Specific Data

اطلاعات نوع خاص برای کدک Windows Media Audio در قالب زیر به عنوان بخشی از Type-Specific Data شیء Stream Properties ذخیره می شود.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## منابع

* [نمایش کلی ASF - مایکروسافت](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


