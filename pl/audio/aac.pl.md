{
  "date" : "2019-12-13",
  "keywords" :["AAC", "plik", "rozszerzenie", "format", "Kodowanie audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku AAC i interfejsy API, które mogą tworzyć i otwierać pliki AAC.",
  "title" :"AAC - zaawansowany plik kodowania audio",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## Czym jest plik AAC?

AAC (Advanced Audio Coding) odnosi się do cyfrowego standardu kodowania dźwięku, który reprezentuje pliki audio w oparciu o stratną kompresję dźwięku. Został on uruchomiony jako następca formatu plików **[MP3](/pl/audio/mp3/)** mając na uwadze, że boczne napotkały problemy związane z wdrażaniem nowych pomysłów w procesie kodowania w oparciu o rozwój metod kompresji danych. AAC zapewnia lepszą jakość dźwięku w porównaniu z MP3 przy tej samej przepływności. Został zdefiniowany w MPEG-2 Part 7 (ISO/IEC 13818-7) oraz w zaktualizowanej formie w MPEG-4 Part 3 (ISO/IEC 14496-3).

Format AAC został przyjęty jako domyślny format multimediów przez YouTube, iPhone'a, iPoda, iPada, Apple iTunes i kilka innych platform. Dostępnych jest kilka aplikacji i interfejsów API do konwersji formatu pliku AAC na inne formaty, takie jak MP3, WMA, M4A, **[WAV](/pl/audio/wav/)** i inne.

### Krótka historia pliku AAC

Format pliku AAC to ulepszona wersja MP3 z pewnymi ulepszeniami. Wniesiony przez kilka firm, w tym Instytut Fraunhofera (Fraunhofer IIS — twórcy MP3), Nokia, Dolby, AT&T i Sony, format ten został uznany za międzynarodowy standard przez Moving Picture Experts Group (MPEG) w kwietniu 1997 r. Później w 1999 r. MPEG-2 część 7 została zaktualizowana i włączona do rodziny standardów MPEG-4. Znany był jako MPEG-4 Part 3, identyfikowany jako ISO/IEC 14496-3: 1999 lub MPEG-4 Audio.

## Specyfikacje formatu plików AAC

Specyfikacje formatu plików AAC pozwalają na większą elastyczność projektowania kodeków niż MP3, co skutkuje większą liczbą równoczesnych strategii kodowania i wydajniejszą kompresją. Format został wybrany przez wiele platform sprzętowych ze względu na jego ulepszenia w stosunku do MP3 pod względem zapewnienia obsługi większej liczby opcji, nawet przy mniejszych przepływnościach. Specyfikacje formatu plików AAC są dostępne jako [MPEG-2 część 7](https://www.iso.org/standard/43345.html) i [MPEG-4 część 3](https://www.iso.org /standard/53943.html) (nie do ściągnięcia za darmo). Format wykorzystuje następujące typy mediów:

* audio/aac
* audio/akp
* audio/3gpp
* audio/3gpp2
* dźwięk/mp4
* audio/mp4a-latm
* audio/mpeg4-ogólne

## AAC vs MP3 - Ulepszenia ##

Główne różnice między AAC i MP3 pod względem ulepszeń są następujące:

* AAC obsługuje szerszy zakres kanałów (do 48) i częstotliwości próbkowania (od 8 kHz do 96 kHz)
* AAC ma lepsze częstotliwości kodowania powyżej 16 kHz
* AAC ma szersze granice zmienności w rozdzielczości częstotliwościowo-czasowej banku filtrów, które doprowadziły do ulepszonego kodowania transjentów i nieruchomych części sygnału audio
* Wydajniejszy i prostszy bank filtrów: hybrydowy bank filtrów został zastąpiony standardowym MDCT (zmodyfikowana dyskretna transformata kosinusowa)
* Obsługuje zwiększoną efektywność kompresji przy użyciu Temporal Noise Shaping (TNS), współczynników predykcji czasu MDCT (predykcja długoterminowa), parametrycznego stereo, percepcyjnego zastępowania szumu, replikacji pasma widmowego (SBR).
* bardziej elastyczne złącze stereo (różne metody mogą być stosowane w różnych zakresach częstotliwości);

## Bibliografia ##

* [AAC – z Wikipedii](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

