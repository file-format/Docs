{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "plik", "rozszerzenie", "format", "co to jest plik amr", "muzyka", "format pliku amr", "plik amr", "konwertuj plik amr na mp3", "odtwórz plik amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku AMR i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki AMR.",
  "title" :"AMR - Adaptacyjny plik kodeków o wielu szybkościach",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Czym jest plik AMR?
Plik z rozszerzeniem .amr to format danych audio odpowiedni dla kodeka audio **Adaptive Multi-Rate**; składa się z wąskopasmowego kodeka mowy o wielu przepływnościach, który koduje sygnały wąskopasmowe z przepływnością 4,75-12,2 kbit/s przy płatnej jakości mowy zaczynającej się od 7,4 kbit/s; wykorzystuje adaptację łącza, aby wybrać jedną z ośmiu różnych szybkości transmisji.

## Format pliku AMR
Format pliku AMR wykorzystuje wiele technik kodowania, algorytm ACELP (Algebraic Code Excited Linear Prediction) jest jedną z najlepszych technik; zaprojektowany do bardziej wydajnej kompresji dźwięku mówionego przez człowieka. AMR został ustawiony jako standardowy kodek głosowy lub mowy przez 3GPP w 1999 roku. Format pliku AMR jest również używany do przechowywania mówionego dźwięku przy użyciu kodeka audio **Adaptive Multi-Rate**, który jest używany przez wiele smartfonów do przechowywania nagrań przemówienia.

### Struktura formatu pliku
AMR (Adaptive Multi-Rate) to format audio; szeroko stosowany w różnych aplikacjach i urządzeniach mobilnych, zwykle w odtwarzaczach/nagrywarkach audio lub aplikacjach typu VoIP. AMR można dalej sklasyfikować jako:

1. AMR-NB (wąskopasmowy)
2. AMR-WB (szerokopasmowy)

Zwykle AMR odnosi się do AMR-NB. Format pliku AMR ma następującą strukturę:

Każdy plik AMR zawiera 6-bajtowy nagłówek, który rozpoznaje plik jako dźwięk AMR. Ten nagłówek jest zawsze ustawiony na:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Jest to zwykle podobne we wszystkich plikach AMR-NB. Jeśli nagłówek jest zgodny ze standardem, prawdopodobnie plik jest uszkodzony i nie powinien być używany. plik AMR składa się z całej liczby spakowanych klatek audio. Każda z tych ramek składa się z 20 ms dźwięku. Każda ramka może być zakodowana przy użyciu dowolnego z obowiązujących trybów AMR-NB (0-7, 8 SID w trybie DTX). Ponieważ ramki mogą być kodowane z różnymi przepływnościami, ta typowa metoda nosi nazwę Adaptive Multi-Rate (AMR).
#### Tryby AMR
Poniżej przedstawiono różne tryby AMR i odpowiadające im szybkości transmisji:

|TRYB| STAWKI BITOWE|
---|---|
|0| AMR 4,75 — koduje z szybkością 4,75 kbit/s|
|1 | AMR 5.15 — koduje z szybkością 5,15 kbit/s|
|2 | AMR 5.9 — koduje z szybkością 5,9 kbit/s|
|3 | AMR 6.7 — koduje z szybkością 6,7 kb/s|
|4 | AMR 7.4 — koduje z szybkością 7,4 kbit/s|
|5 | AMR 7,95 — koduje z szybkością 7,95 kbit/s|
|6 | AMR 10.2 — koduje z szybkością 10,2 kb/s|
|7 | AMR 12.2 — koduje z szybkością 12,2 kbit/s|

Rozmiar ramki trybów AMR w bajtach (łącznie z bajtem nagłówka) podano poniżej:

|CMR |TRYB |ROZMIAR RAMKI (w bajtach )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Bibliografia ##

* [Adaptive Multi-Rate audio codec – Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Format ładunku RTP i format przechowywania plików dla kodeków audio AMR i AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

