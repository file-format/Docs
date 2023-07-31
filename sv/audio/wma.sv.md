{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "fil", "tillägg", "format", "ljudutbytesfilformat", "musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om WMA-filformat och API:er som kan skapa och öppna WMA-filer.",
  "title" :"WMA - Windows Media Audio File",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Vad är en WMA fil?

En fil med filtillägget .wma representerar en ljudfil som sparas i formatet Advanced Systems Format (ASF). ASF är Microsofts proprietära format som innehåller bitströmmar kodade av Windows Media Audio 9. Utöver ljudinnehållet innehåller en WMA-fil även metadataobjekt som titel, album, artist och genre för spåret. WMA-filer används främst för streaming över webben som liknar [.mp3](/sv/audio/mp3/)-filer.

## WMA-filformat

En WMA-fil är ett binärt filformat och ingår i ASF-filformatet. Den anger kodningen av metadata om filen som liknar ID3-taggarna som används av MP3-filerna. WMA-codec har använts av Microsoft i dess Protected Interoperable File Format (PIFF) sedan 2008. Den har dock inte deklarerats som standardiserad ljud-codec av relaterade industristandarder som DECE UltraViolet och MPEG-DASH.

### WMA-typspecifika data

Den typspecifika informationen för Windows Media Audio-codec lagras i följande format som en del av typspecifika data för Stream Properties Object.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referenser

* [ASF-översikt - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

