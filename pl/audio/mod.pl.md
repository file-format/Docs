{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "plik", "rozszerzenie", "format", "czym jest format pliku mod", "muzyka", "format pliku mod", "mod vs MP3", "specyfikacja formatu pliku mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku MOD i interfejsach API, które mogą tworzyć, konwertować i otwierać pliki MOD.",
  "title" :"MOD - plik modułu muzycznego",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Czym jest plik MOD?
Plik z rozszerzeniem .mod to plik modułu muzycznego utworzony przy użyciu standardowego formatu modułu muzycznego, który jest oparty na **formacie modułu Amiga** opracowanym przez Karstena Obarskiego i wydanym z oprogramowaniem **Ultimate Soundtracker** dla Commodore systemu Amigi. Podobnie jak plik [MIDI](/pl/audio/mid/), zawiera schematy nut i próbki dźwiękowe reprezentujące różne instrumenty, które są odtwarzane zgodnie z nutami. Pliki MOD są szczególnie używane w grach wideo jako muzyka w tle oraz w subkulturze ** demosceny ** sztuki komputerowej.

## Format pliku MOD

MOD to format pliku komputerowego, którego podstawową funkcją jest reprezentowanie muzyki i był to pierwszy format pliku modułu. Pliki MOD używają rozszerzenia .mod, z wyjątkiem **Amigi**, która odczytuje nagłówek pliku w celu określenia typu pliku, więc nie polega na rozszerzeniach nazw plików. Plik MOD składa się z zestawu różnych instrumentów w postaci sampli, szeregu schematów określających, jak i kiedy próbki mają być odtwarzane, oraz listy, jakie schematy mają być odtwarzane w jakiej kolejności.

### Specyfikacje formatu pliku MOD

Wzorzec pliku MOD jest w rzeczywistości zaprojektowany w interfejsie użytkownika sekwencera jako tabela z jedną kolumną na kanał, więc ta tabela ma cztery kolumny (po jednej dla każdego kanału sprzętowego Amigi. Każda kolumna ma 64 wiersze).

Komórka w tabeli może spowodować wykonanie jednej z następujących akcji na kanale jej kolumny po osiągnięciu czasu jej wiersza:

- Uruchom instrument, grając nową nutę w tym kanale z określoną głośnością, ewentualnie z zastosowanym efektem specjalnym
- Zmień głośność lub efekt specjalny zastosowany do bieżącej notatki
- Zmień przepływ wzoru; przeskoczyć do określonej pozycji utworu lub schematu lub zapętlić się w schemacie
- Nic nie robić; wszelkie nuty grane na tym kanale będą nadal odtwarzane

Instrument to pojedyncza próbka wraz z opcjonalną specyfikacją, która część próbki może zostać powtórzona, aby zachować pełną nutę.

### Wyczucie czasu
Minimalny przedział czasu wynosił 0,02 sekundy w oryginalnym pliku MOD lub interwał „wygaszania pionowego” (VSync), ponieważ oryginalne oprogramowanie wykorzystywało taktowanie VSync monitora pracującego z częstotliwością 50 Hz (dla PAL) lub 60 Hz (dla NTSC) dla czasu.

## Bibliografia

* [MOD (format pliku) - Według Wikipedii](https://en.wikipedia.org/wiki/MOD_(file_format))

