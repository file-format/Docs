{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku TS — plik strumienia transportu wideo",
  "keywords" :[ "ts", "flie", "rozszerzenie", "rozszerzenie", ".ts", "format" ],
  "description":"Dowiedz się, czym jest plik TS i interfejsy API, które mogą tworzyć i otwierać pliki TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Czym jest plik TTS?

Plik z rozszerzeniem .ts to strumień wideo, który przechowuje dane na płytach DVD. Wykorzystuje algorytm kompresji MPEG-2 ([.mpeg](/pl/video/mpg/)), aby osiągnąć maksymalną wydajność i kompatybilność z różnymi typami mediów, takimi jak transmisje strumieniowe i transmisje internetowe. Format pliku TS został stworzony, aby można go było odtwarzać na urządzeniach o słabym połączeniu internetowym, takich jak smart TV.

## Format pliku TS — więcej informacji

Dane w pliku TS są podobne do pliku [MP4](/pl/video/mp4/), ale są podzielone na małe fragmenty. Każdy fragment składa się z małego fragmentu wideo, po którym następuje fragment dźwięku i opcjonalny podpis. Pojedynczy plik TS składa się z wielu takich fragmentów. Oprócz wideo, audio i napisów, każdy fragment zawiera również dodatkowe dane do wykrywania błędów w fragmencie. Z tego powodu pliki TS mają nieco większy rozmiar.

### Dlaczego warto używać formatu plików TS?

Jeśli więc pliki TS są dość duże, jaką korzyść daje ich użycie zamiast innych formatów plików? Cóż, w przypadku nadawania maleńkie fragmenty obrazu i dźwięku mogą być przesyłane przez media komunikacyjne (przewodowe lub radiowe) w czasie rzeczywistym. Dodatkowe dane w porcjach są wykorzystywane przez odbiornik do pominięcia porcji podatnych na błędy.

Ponadto używane są pliki TS, ponieważ system nadawczy nie potrzebuje całego strumienia, aby go odtworzyć. Transmisję można odebrać i wykorzystać w czasie rzeczywistym poprzez złożenie audio i wideo.

## Jak odtwarzać pliki TS?

Cóż, pliki TS można otwierać i odtwarzać w popularnym [odtwarzaczu multimedialnym VideoLAN VLC](https://www.videolan.org/vlc/features.html), który jest bezpłatnie dostępny do pobrania.

## Bibliografia ##

* [Strumień transportowy MPEG – Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)

