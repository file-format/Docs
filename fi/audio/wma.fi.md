{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"tiedosto",
"laajennus",
"muoto",
"äänenvaihdon tiedostomuoto",
"musiikkia"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WMA-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WMA-tiedostoja.",
  "title": "WMA - Windows Media -äänitiedosto",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-fia"
}
},
  "lastmod": "2021-02-20"
}

## Mikä on WMA-tiedosto?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Äänisisällön lisäksi WMA-tiedosto sisältää myös metatietoobjekteja, kuten kappaleen nimen, albumin, esittäjän ja genren. WMA-tiedostoja käytetään ensisijaisesti suoratoistoon verkossa, kuten [.mp3](/audio/mp3/)-tiedostoja.

## WMA tiedostomuoto

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Sitä ei kuitenkaan ole julistettu standardisoiduksi audiokoodekiksi liittyvissä alan standardeissa, kuten DECE UltraViolet ja MPEG-DASH.

### WMA-tyyppikohtaiset tiedot

Windows Media Audio -koodekin tyyppikohtaiset tiedot tallennetaan seuraavassa muodossa osana Stream Properties -objektin tyyppikohtaisia tietoja.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Viitteet

* [ASF Overview – Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


