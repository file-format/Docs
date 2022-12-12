{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "soubor", "přípona", "formát", "formát souboru pro výměnu zvuku", "hudba" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů WMA a rozhraních API, která mohou vytvářet a otevírat soubory WMA.",
  "title" :"WMA - Windows Media Audio File",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Co je soubor WMA?

Soubor s příponou .wma představuje zvukový soubor, který je uložen ve formátu ASF (Advanced Systems Format). ASF je proprietární formát společnosti Microsoft, který obsahuje bitové toky kódované systémem Windows Media Audio 9. Kromě zvukového obsahu obsahuje soubor WMA také objekty metadat, jako je název, album, interpret a žánr skladby. Soubory WMA se primárně používají pro streamování přes web podobně jako soubory [.mp3](/cs/audio/mp3/).

## Formát souboru WMA

Soubor WMA je binární formát souboru a je obsažen ve formátu souboru ASF. Specifikuje kódování metadat o souboru podobně jako ID3 tagy používané soubory MP3. Kodek WMA používá společnost Microsoft ve svém chráněném interoperabilním formátu souborů (PIFF) od roku 2008. Nebyl však deklarován jako standardizovaný zvukový kodek souvisejícími průmyslovými standardy, jako jsou DECE UltraViolet a MPEG-DASH.

### Specifická data typu WMA

Typově specifické informace pro kodek Windows Media Audio jsou uloženy v následujícím formátu jako součást Typově specifických dat objektu Stream Properties.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Reference

* [Přehled ASF – Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

