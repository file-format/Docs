{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"fayl",
"uzadılması",
"format",
"audio mübadilə fayl formatı",
"musiqi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "WMA fayl formatı və WMA faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "WMA - Windows Media Audio Faylı",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-aza"
}
},
  "lastmod": "2021-02-20"
}

## WMA faylı nədir?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Audio məzmuna əlavə olaraq, WMA faylı həmçinin başlıq, albom, ifaçı və trekin janrı kimi metadata obyektlərini ehtiva edir. WMA faylları ilk növbədə [.mp3](/audio/mp3/) fayllarına bənzər veb üzərindən axın etmək üçün istifadə olunur.

## WMA fayl formatı

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Bununla belə, DECE UltraViolet və MPEG-DASH kimi müvafiq sənaye standartları tərəfindən standartlaşdırılmış audio kodek kimi elan edilməmişdir.

### WMA Tipi Xüsusi Məlumat

Windows Media Audio kodek üçün növə aid məlumat Yayım Xüsusiyyətləri Obyektinin Tip Xüsusi Məlumatının bir hissəsi kimi aşağıdakı formatda saxlanılır.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## İstinadlar

* [ASF İcmal - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


