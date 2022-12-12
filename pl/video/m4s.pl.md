{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik M4S - Co to jest plik M4S?",
  "description":"Poznaj format plików M4S i interfejsy API, które mogą tworzyć i otwierać pliki M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Czym jest plik M4S?

Plik M4S to mały fragment filmu przesyłanego strumieniowo przez Internet przy użyciu techniki przesyłania strumieniowego **MPEG-DASH**. Zawiera segment wideo w postaci danych binarnych. Aplikacja odbierająca (zwykle przeglądarka internetowa lub odtwarzacze multimedialne) odtwarza te segmenty w kolejności ich odebrania. Pierwszy segment M4S jest identyfikowany przez zawarte w nim dane inicjalizacyjne. W **podsumowaniu** pliki M4S to małe pojedyncze segmenty multimedialne całego pliku.

## Format pliku M4S

Pliki M4S są oparte na [formacie ISO Base Media File (ISOBMFF)] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Te małe segmenty dużego pliku można pobrać niezależnie za pośrednictwem protokołu HTTP. Tak więc, jeśli masz duży plik filmowy [MP4](/pl/video/mp4/), można go przesyłać strumieniowo przy użyciu techniki MPEG-DASH (Dynamic Adaptive Streaming over HTTP), dzieląc go na segmenty plików M4S. Jeśli ten duży plik filmowy zostanie pobrany na dysk jako M4S, zostanie pobranych wiele plików M4S. Jeśli wszystkie te segmenty .m4s zostaną połączone, zostanie utworzony kompletny plik, który można odtworzyć. Odtwarzacze multimedialne nie mogą odtworzyć pliku, chyba że w pliku jest również dostępny pierwszy segment inicjujący.

## Informacje o strumieniowaniu MPEG-DASH

MPEG-DASH wykorzystuje technikę przesyłania strumieniowego z adaptacyjną szybkością transmisji bitów, która umożliwia strumieniowe przesyłanie wysokiej jakości treści multimedialnych przez Internet. Odbywa się to poprzez podzielenie treści na sekwencję małych segmentów, które są przesyłane strumieniowo przez HTTP. W ten sposób można przesyłać strumieniowo duże pliki multimedialne, takie jak filmy, podcasty lub transmisje na żywo z wydarzeń sportowych. Segmenty te są kodowane z różnymi przepływnościami. Odtwarzacze multimediów obsługujące MPEG-DASH automatycznie wybierają segment o najwyższej przepływności za pomocą algorytmu adaptacji szybkości transmisji. Pozwala to uniknąć przeciągania lub ponownego buforowania zdarzeń podczas odtwarzania.

### Open-Source API dla plików M4S

Dostępne są interfejsy API typu open source, których można używać do odczytywania i konwertowania plików M4S.

* [libdash](https://github.com/bitmovin/libdash) - API .NET dla plików M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Klient JavaScript dla pliku M4S
* [Biblioteka Go do tworzenia plików Dash](https://github.com/zencoder/go-dash)

### Interfejs API typu open source do konwersji M4S na MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Bibliografia ###

* [format ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming przez HTTP – MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

