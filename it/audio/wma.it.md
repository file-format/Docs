{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "file", "estensione", "formato", "formato file di interscambio audio", "musica" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file WMA e le API che possono creare e aprire file WMA.",
  "title" :"WMA - File audio Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Che cos'è un file WMA?

Un file con estensione .wma rappresenta un file audio salvato nel formato ASF (Advanced Systems Format). ASF è il formato proprietario di Microsoft che contiene flussi di bit codificati da Windows Media Audio 9. Oltre al contenuto audio, un file WMA contiene anche oggetti di metadati come titolo, album, artista e genere del brano. I file WMA vengono utilizzati principalmente per lo streaming sul Web in modo simile ai file [.mp3](/it/audio/mp3/).

## Formato file WMA

Un file WMA è un formato di file binario ed è contenuto nel formato di file ASF. Specifica la codifica dei metadati sul file simile ai tag ID3 utilizzati dai file MP3. Il codec WMA è stato utilizzato da Microsoft nel suo Protected Interoperable File Format (PIFF) dal 2008. Tuttavia, non è stato dichiarato codec audio standardizzato dagli standard di settore correlati come DECE UltraViolet e MPEG-DASH.

### Dati specifici del tipo WMA

Le informazioni specifiche sul tipo per il codec Windows Media Audio vengono archiviate nel formato seguente come parte dei dati specifici del tipo dell'oggetto Stream Properties.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Riferimenti

* [Panoramica ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

