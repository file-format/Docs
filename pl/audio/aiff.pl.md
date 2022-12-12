{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "plik", "rozszerzenie", "format", "format pliku wymiany audio", "muzyka", "format pliku aiff", "aiff na mp3", "aiff vs wav", "konwertuj aiff na mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku AIFF i interfejsy API, które mogą tworzyć, konwertować i otwierać pliki AIFF.",
  "title" :"AIFF — format pliku wymiany audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Czym jest plik AIFF?
AIFF (Audio Interchange File Format) to nieskompresowany format plików audio opracowany przez Apple w 1998 roku, ale oparty na **EA IFF 85** (Standard for Interchange Format Files opracowany przez Electronic Arts), formacie opakowania używanym w systemach Amiga . Ten format pliku zawiera standard przechowywania samplowanych dźwięków. Format jest wystarczająco elastyczny i umożliwia przechowywanie samplowanych dźwięków monofonicznych lub wielokanałowych przy różnych częstotliwościach próbkowania i szerokościach próbkowania. Ponieważ pliki AIFF są nieskompresowane, ta rzecz sprawia, że mają większy rozmiar niż inne formaty stratne, takie jak [MP3](https://docs.fileformat.com/audio/mp3/).

Pliki AIFF składają się z 2 kanałów nieskompresowanego dźwięku stereo z 16-bitowym rozmiarem próbki, nagranego z częstotliwością 44,1 kHz. Ze względu na wysoką jakość dźwięku 5-minutowy dźwięk może zająć do 50 MB miejsca na dysku, co odpowiada formatowi pliku [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF kontra WAV

AIFF i WAV są prawie takie same pod względem jakości. Oba używają tego samego kodowania PCM (modulacja impulsowo-kodowa), co czyni je większymi w porównaniu z innymi formatami stratnymi, takimi jak [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Niektóre z ogólnych różnic przedstawiono w poniższej tabeli:

|AIFF|WAV|
---|---|
|Używany głównie dla komputerów Mac|Głównie używany dla komputerów PC|
|Pozwala na metadane| Nie pozwala na metadeta|

## Struktura plików AIFF

**EA IFF 85** określa ogólną strukturę przechowywania danych w plikach. Plik **EA IFF 85** składa się z wielu porcji danych. Blok budulcowy pliku AIFF składa się z informacji nagłówka, po których następują dane:
{{< figure src="../chunk.png" alt="Kawałek AIFF" >}}

Plik AIFF to zbiór wielu różnych typów fragmentów. Istnieją dwa ogólne typy fragmentów, które są ważne przy tworzeniu fragmentu pliku AIFF:
- **Common Chunk**: Zawiera ważne parametry opisujące samplowany dźwięk, takie jak jego długość i częstotliwość próbkowania.
- **Sound Data Chunk**: Zawiera rzeczywiste próbki audio.
Istnieje wiele innych opcjonalnych fragmentów, które zawierają listę parametrów instrumentu, definiują znaczniki, przechowują informacje specyficzne dla aplikacji itp.

### Lokalne typy fragmentów

Typy fragmentów do utworzenia AIFF podano w poniższej tabeli:

|Typ kawałka| Opis|
---|---|
|Common Chunk|Common Chunk opisuje podstawowe parametry samplowanego dźwięku|
|Sound Data Chunk|Sound Data Chunk zawiera rzeczywiste klatki sampli|
|Marker Chunk|Marker Chunk zawiera znaczniki wskazujące pozycje w danych dźwiękowych|
|Instrument Chunk|Instrument Chunk definiuje podstawowe parametry, których instrument, taki jak sampler, może użyć do odtwarzania danych dźwiękowych|
|MIDI Data Chunk|MIDI Data Chunk może być używany do przechowywania danych MIDI|
|Fragment nagrania audio|Fragment nagrania audio zawiera informacje dotyczące urządzeń do nagrywania dźwięku|
|Application Specific Chunk|Application Specific Chunk może być używany do dowolnych celów przez producentów aplikacji|
|Comments Chunk|Comments Chunk służy do przechowywania komentarzy w FORMULARZU AIFF|
|Fragmenty tekstu — nazwa, autor, prawa autorskie, adnotacje| Wszystkie są kawałkami tekstu|

## Bibliografia ##

* [Format pliku wymiany audio – według Wikipedii](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

