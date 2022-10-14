{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "Datei", "Erweiterung", "Format", "Audio Interchange File Format", "Musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das WMA-Dateiformat und APIs, die WMA-Dateien erstellen und öffnen können.",
  "title" :"WMA - Windows Media-Audiodatei",
  "linktitle" :"WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Was ist eine WMA-Datei?

Eine Datei mit der Erweiterung .wma stellt eine Audiodatei dar, die im Advanced Systems Format (ASF)-Format gespeichert ist. ASF ist das proprietäre Format von Microsoft, das von Windows Media Audio 9 codierte Bitstreams enthält. Zusätzlich zum Audioinhalt enthält eine WMA-Datei auch Metadatenobjekte wie Titel, Album, Interpret und Genre des Tracks. WMA-Dateien werden hauptsächlich zum Streamen über das Internet verwendet, ähnlich wie [.mp3](/de/audio/mp3/)-Dateien.

## WMA-Dateiformat

Eine WMA-Datei ist ein binäres Dateiformat und ist im ASF-Dateiformat enthalten. Es gibt die Codierung von Metadaten über die Datei ähnlich den ID3-Tags an, die von den MP3-Dateien verwendet werden. Der WMA-Codec wird seit 2008 von Microsoft in seinem geschützten interoperablen Dateiformat (PIFF) verwendet. Er wurde jedoch von den verwandten Industriestandards wie DECE UltraViolet und MPEG-DASH nicht als standardisierter Audiocodec deklariert.

### WMA-typspezifische Daten

Die typspezifischen Informationen für den Windows Media Audio-Codec werden im folgenden Format als Teil der typspezifischen Daten des Stream-Eigenschaftenobjekts gespeichert.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Verweise

* [ASF-Übersicht – Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

