{
  "date" : "2021-02-20",
  "keywords" :["WMA", "plik", "rozszerzenie", "format", "format pliku wymiany audio", "muzyka"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików WMA i interfejsy API, które mogą tworzyć i otwierać pliki WMA.",
  "title" :"WMA — plik Windows Media Audio",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Czym jest plik WMA?

Plik z rozszerzeniem .wma reprezentuje plik audio zapisany w formacie Advanced Systems Format (ASF). ASF to zastrzeżony format firmy Microsoft, który zawiera strumienie bitów zakodowane przez Windows Media Audio 9. Oprócz treści audio plik WMA zawiera również obiekty metadanych, takie jak tytuł, album, wykonawca i gatunek utworu. Pliki WMA są używane głównie do przesyłania strumieniowego przez Internet, podobnie jak pliki [.mp3](/pl/audio/mp3/).

## Format pliku WMA

Plik WMA jest formatem pliku binarnego i jest zawarty w formacie pliku ASF. Określa kodowanie metadanych dotyczących pliku, podobnie jak znaczniki ID3 używane w plikach MP3. Kodek WMA jest używany przez firmę Microsoft w Protected Interoperable File Format (PIFF) od 2008 roku. Jednak nie został uznany za standardowy kodek audio przez powiązane standardy branżowe, takie jak DECE UltraViolet i MPEG-DASH.

### Dane specyficzne dla typu WMA

Informacje specyficzne dla typu kodera-dekodera Windows Media Audio są przechowywane w następującym formacie jako część danych specyficznych dla typu obiektu Właściwości strumienia.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Bibliografia

* [Omówienie ASF — Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

