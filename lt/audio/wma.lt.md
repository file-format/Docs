{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"failą",
"pratęsimas",
"formatu",
"garso mainų failo formatas",
"muzika"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WMA failo formatą ir API, kurios gali kurti ir atidaryti WMA failus.",
  "title": "WMA – „Windows Media“ garso failas",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-lta"
}
},
  "lastmod": "2021-02-20"
}

## Kas yra WMA failas?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Be garso turinio, WMA faile taip pat yra metaduomenų objektų, tokių kaip pavadinimas, albumas, atlikėjas ir takelio žanras. WMA failai pirmiausia naudojami srautiniam perdavimui internete, panašiai kaip [.mp3](/audio/mp3/) failai.

## WMA failo formatas

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Tačiau jis nebuvo paskelbtas standartizuotu garso kodeku pagal susijusius pramonės standartus, tokius kaip DECE UltraViolet ir MPEG-DASH.

### Specifiniai WMA tipo duomenys

Windows Media garso kodeko tipui būdinga informacija saugoma tokiu formatu kaip srauto ypatybių objekto tipui būdingų duomenų dalis.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Nuorodos

* [ASF apžvalga – „Microsoft“](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


