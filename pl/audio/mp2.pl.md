{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "plik mp2", "rozszerzenie", "format", "co to jest plik mp2", "muzyka", "format pliku mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików MP2 i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki MP2.",
  "title" :"MP2 - Format pliku audio MPEG Layer 2",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Co to jest plik MP2?

Plik MP2, który jest również nazywany plikiem MPA, to plik audio skompresowany z warstwą II MPEG-1 lub MPEG-2; stratny format kompresji audio zdefiniowany przez ISO/IEC 11172-3 wraz z MPEG-1 Audio Layer I i MPEG-1 Audio Layer III ([MP3](/pl/audio/mp3/)), aby zmniejszyć rozmiar pliku audio. Podczas gdy MP3 jest bardziej popularny niż MP2 ze względu na mniejszy rozmiar i dostępność w Internecie. Dlatego MP2 jest nadal podstawowym standardem transmisji audio.

## Format pliku MP2

MPEG Audio Layer II (MP2) to podstawowy algorytm standardów MP3. Kodowanie MPEG-1 Audio Layer 2 uzyskano z kodeka audio MUSICAM. Zaczęło się od projektu Digital Audio Broadcast (DAB) w Niemczech w ramach programu badawczego EUREKA. Eureka 147 zawierała trzy główne elementy: kodowanie i multipleksowanie transmisji, modulację COFDM i kodowanie dźwięku MUSICAM (wzorzec maskowania Universal Sub-band Integrated Coding And Multiplexing). MUSICAM był jednym z nielicznych kodowań, które były w stanie osiągnąć wysoką jakość dźwięku przy przepływności w zakresie od 64 do 192 kbit/s na kanał monofoniczny. Celem było zapewnienie małych opóźnień, niskiej złożoności, odporności na błędy, jednostek o krótkim dostępie oraz spełnienia wymagań technicznych związanych z nadawaniem, telekomunikacją i nagrywaniem na cyfrowych nośnikach danych.

MP2 to podpasmowy koder audio, który może kompresować w domenie czasu z bankiem filtrów o niskim opóźnieniu, generującym 32 komponenty w domenie częstotliwości. Dla porównania, MP3 to koder audio z transformacją z hybrydowym bankiem filtrów, co oznacza, że kompresja jest stosowana w dziedzinie częstotliwości po hybrydowej transformacji z dziedziny czasu. Koder MP2 może wykorzystywać redundancje międzykanałowe przy użyciu opcjonalnego kodowania intensywności „joint stereo”.

### Specyfikacje formatu plików MP2

Format pliku MP2 oparty jest na kolejnych klatkach cyfrowych o 1152 interwałach próbkowania z czterema możliwymi formatami:

-format mono
- format stereo
- zakodowany intensywność wspólnego formatu stereo (nieistotność stereo)
- format dwukanałowy (nieskorelowany).
Niektóre ważne specyfikacje techniczne MP2 podano w poniższej tabeli:

|Specyfikacja| Opis|
---|---|
|**Częstotliwości próbkowania**| 32, 44,1 i 48 kHz|
|**Przepustowość**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 i 384 kbit/s|
|**Dodatkowe częstotliwości próbkowania**|16, 22,05 i 24 kHz|
|**Dodatkowe szybkości transmisji**|8, 16, 24, 40 i 144 kbit/s|
|**Wsparcie wielokanałowe**|Do 5 pełnozakresowych kanałów audio i kanał LFE (Low Frequency Enhancement)|

## Bibliografia ##

* [MPEG-1 Audio Layer II – z Wikipedii](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

