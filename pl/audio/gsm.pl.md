{
  "date" : "2021-08-05",
  "keywords" :["gsm", "plik", "rozszerzenie", "format", "Audio", "Global System for Mobile Audio", "rozszerzenie gsm", "pliki gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików GSM i interfejsy API, które mogą tworzyć i otwierać pliki GSM.",
  "title" :"GSM – Globalny System Mobilnego Formatu Plików Audio",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Czym jest plik GSM?

GSM to rozszerzenie pliku powiązane z Global System for Mobile Audio Format Files. Pliki zawierające rozszerzenia GSM można otwierać na platformach Linux, Windows i Mac OS. Format plików GSM należy do kategorii plików dźwiękowych.

Plik GSM jest kodowany przy użyciu stratnego kodeka kompresji dźwięku CBR (Constant bitrate). Częstotliwość próbkowania w pliku audio GSM wynosi 8000 próbek na sekundę, podczas gdy szybkość transmisji danych wynosi około 13 kb/s. Szybkość transmisji w plikach GSM zapewnia jakość podczas nagrywania głosu. Ponadto format pliku GSM jest również znany jako globalny standardowy format używany w telefonach komórkowych, a pliki WAV można również łatwo zakodować przy użyciu formatu pliku GSM. Wszelkie problemy z plikiem GSM użytkownik może łatwo rozwiązać samodzielnie, bez konieczności wizyty u specjalisty.

Użytkownicy mogą również konwertować pliki GSM do formatów [MP3](/pl/audio/mp3/) i [MP4](/pl/audio/mp4/).

## Krótka historia formatu plików GSM

GSM to format pliku audio, który został stworzony dla telefonii internetowej w Europie. Został opracowany przez Europejski Instytut Norm Telekomunikacyjnych (ETSI) do użytku jako cyfrowa komórka 2G używana w telefonach komórkowych i tabletach. Dziś służy do przechowywania nagrań rozmów telefonicznych i komunikatów głosowych.

## Specyfikacje formatu plików GSM ##

GSM działa w sieci strukturalnej, która składa się z następujących sekcji:

- **Modulacja**: Jest to proces przekształcania danych wejściowych do formatu, który można łatwo przesłać. Przesyłane dane są demodulowane po stronie odbierającej
- **Szybkość transmisji** : GSM to system cyfrowy, który ma szybkość transmisji ponad 270 kb/s
- **Zakres częstotliwości łącza wysyłającego** : 933-960 MHz
- **Zakres częstotliwości łącza w dół**: 890 – 915 MHz
- **Odstęp między kanałami**: Oznacza odstęp między sąsiednimi barierami, który powinien wynosić około 200 kHz
- **Odległość dupleksowa**: Jest to odstęp między częstotliwościami łącza w górę i łącza w dół, który powinien wynosić 80 MHz
- **Kodowanie mowy**: GSM używa liniowego kodowania predykcyjnego (LPC). LPC kompresuje przepływność. Kiedy sygnał dźwiękowy przechodzi przez filtr i naśladuje trakt głosowy. GSM koduje mowę z szybkością 13 kb/s

| Format kompresji dźwięku | algorytm | Częstotliwość próbkowania | Transformacja szybkości transmisji | opóźnienie | CBR | VBR | stereo | Wielokanałowy |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8kHz | 5,6 kb/s | 25 ms | Tak | Nie | Nie | Nie |
| GSM-FR | RPE-LTP | 8kHz | 13 kbit/s | 20–30 ms | Tak | Nie | Nie | Nie |
| GSM-EFR | ACELP | 8kHz | 12,2 kb/s | 20–30 ms | Tak | Nie | Nie | Nie |

## Bibliografia ##

* [GSM – z Wikipedii](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

