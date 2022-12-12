{
  "date" : "2019-12-13",
  "keywords" :["WAV", "plik", "rozszerzenie", "format", "format pliku wymiany audio", "muzyka"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików WAV i interfejsy API, które mogą tworzyć i otwierać pliki WAV.",
  "title" :"WAV - Waveform Audio File Format",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Czym jest plik WAV?

WAV, znany jako WAVE (Waveform Audio File Format), jest podzbiorem specyfikacji Microsoft Resource Interchange File Format (RIFF) do przechowywania cyfrowych plików audio. Format nie stosuje żadnej kompresji do strumienia bitów i przechowuje nagrania audio z różnymi częstotliwościami próbkowania i przepływnościami. Był i jest jednym ze standardowych formatów płyt audio CD. Pliki Wave mają większy rozmiar w porównaniu z nowymi formatami plików audio, takimi jak [MP3](/pl/audio/mp3/), które wykorzystują kompresję stratną w celu zmniejszenia rozmiaru pliku przy zachowaniu tej samej jakości dźwięku. Jednak pliki WAV można kompresować przy użyciu kodeków Audio Compression Manager (ACM). Dostępnych jest kilka interfejsów API i aplikacji, które mogą konwertować pliki WAV na inne popularne formaty plików audio.

**Czy wiedziałeś?**
Możesz zostać współtwórcą w FileFormat.com, aby społeczność formatów plików była na bieżąco ze swoimi odkryciami. Jeśli chcesz podzielić się czymś na temat formatów plików WAV lub audio, możesz opublikować swoje odkrycia w sekcji [Audio File Format News](https://news.fileformat.com/t/audio), aby ludzie byli na bieżąco.

## Format pliku WAV ##

Format pliku WAVE, będący podzbiorem specyfikacji RIFF firmy Microsoft, zaczyna się od nagłówka pliku, po którym następuje sekwencja fragmentów danych. Plik WAVE ma pojedynczą porcję „WAVE”, która składa się z dwóch części podrzędnych:

* fragment "fmt" - określa format danych
* fragment „danych” — zawiera rzeczywiste przykładowe dane

### Nagłówek pliku WAV ###

Nagłówek pliku WAV (RIFF) ma długość 44 bajtów i ma następujący format:


|Pozycje|Przykładowa wartość|Opis
---|---|---|
|1 - 4|"RIFF"|Oznacza plik jako riff. Znaki mają długość 1 bajta.
|5 - 8|Rozmiar pliku (liczba całkowita)|Rozmiar całego pliku - 8 bajtów, w bajtach (32-bitowa liczba całkowita). Zwykle wypełniasz to po utworzeniu.
|9 -12|"WAVE"|Nagłówek typu pliku. Dla naszych celów zawsze równa się „FALA”.
|13-16|"fmt "|Formatuj znacznik porcji. Zawiera końcową wartość null
|17-20|16|Długość formatu danych jak podano powyżej
|21-22|1|Typ formatu (1 to PCM) - 2-bajtowa liczba całkowita
|23-24|2|Liczba kanałów - 2-bajtowa liczba całkowita
|25-28|44100|Częstotliwość próbkowania - 32-bajtowa liczba całkowita. Typowe wartości to 44100 (CD), 48000 (DAT). Częstotliwość próbkowania = liczba próbek na sekundę lub Hertz.
|29-32|176400|(częstotliwość próbkowania * liczba bitów na próbkę * kanały) / 8.
|33-34|4|(BitsPerSample * Kanały) / 8.1 — 8 bitów mono2 — 8 bitów stereo/16 bitów mono4 — 16 bitów stereo
|35-36|16|Bity na próbkę
|37-40|"dane"|nagłówek fragmentu "dane". Oznacza początek sekcji danych.
|41-44|Rozmiar pliku (dane)|Rozmiar sekcji danych.
|Powyżej podano przykładowe wartości dla 16-bitowego źródła stereo.

## Bibliografia ##

* [WAV – z Wikipedii](https://en.wikipedia.org/wiki/WAV)

