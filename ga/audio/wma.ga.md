{
  "date": "2021-02-20",
  "keywords": [
"WMA",
"comhad",
"síneadh",
"formáid",
"formáid comhaid idirmhalartaithe fuaime",
"Ceol"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid WMA agus APIs is féidir comhaid WMA a chruthú agus a oscailt.",
  "title": "WMA - Comhad Fuaime Windows Media",
  "linktitle": "WMA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wm-gaa"
}
},
  "lastmod": "2021-02-20"
}

## Cad is comhad WMA ann?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. Chomh maith leis an ábhar fuaime, tá comhad WMA freisin rudaí meiteashonraí ar nós teideal, albam, ealaíontóir, agus seánra an rian. Úsáidtear comhaid WMA go príomha le haghaidh sruthú thar an ngréasán cosúil le comhaid [.mp3](/audio/mp3/).

## Formáid Comhaid WMA

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. Mar sin féin, níl sé dearbhaithe mar chód fuaime caighdeánaithe ag na caighdeáin tionscail ghaolmhara ar nós DECE UltraViolet agus MPEG-DASH.

### WMA Cineál Sonraí Sonracha

Stóráiltear an fhaisnéis a bhaineann go sonrach le haghaidh an chódaigh Windows Media Audio san fhormáid seo a leanas mar chuid de Shonraí Cineál-Shonracha an tSrutha Réada Airíonna.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Tagairtí

* [Forbhreathnú ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


