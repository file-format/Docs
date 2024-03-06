{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"failu",
"pagarinājumu",
"formātā",
"audio apmaiņas faila formāts",
"mūzika"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WMA failu formātu un API, kas var izveidot un atvērt WMA failus.",
  "title": "WMA — Windows Media audio fails",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-lva"
}
},
  "lastmod": "2021-02-20"
}

## Kas ir WMA fails?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Papildus audio saturam WMA failā ir arī metadatu objekti, piemēram, ieraksta nosaukums, albums, izpildītājs un žanrs. WMA faili galvenokārt tiek izmantoti straumēšanai tīmeklī, līdzīgi kā [.mp3](/audio/mp3/) faili.

## WMA faila formāts

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Tomēr saistītajos nozares standartos, piemēram, DECE UltraViolet un MPEG-DASH, tas nav pasludināts par standartizētu audio kodeku.

### WMA tipa specifiskie dati

Tipam specifiskā informācija Windows Media Audio kodekam tiek glabāta tālāk norādītajā formātā kā daļa no straumes rekvizītu objekta tipa specifiskajiem datiem.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Atsauces

* [ASF pārskats — Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


