{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"fil",
"udvidelse",
"format",
"lydudvekslingsfilformat",
"musik"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WMA-filformat og API'er, der kan oprette og åbne WMA-filer.",
  "title": "WMA - Windows Media Audio File",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-daa"
}
},
  "lastmod": "2021-02-20"
}

## What is a WMA file?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Ud over lydindholdet indeholder en WMA-fil også metadataobjekter såsom titel, album, kunstner og sporets genre. WMA-filer bruges primært til streaming over nettet svarende til [.mp3](/audio/mp3/) filer.

## WMA filformat

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Det er dog ikke blevet erklæret som standardiseret audio-codec af de relaterede industristandarder såsom DECE UltraViolet og MPEG-DASH.

### WMA-typespecifikke data

De typespecifikke oplysninger for Windows Media Audio-codec'et gemmes i følgende format som en del af de typespecifikke data for Stream Properties Object.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referencer

* [ASF-oversigt - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


