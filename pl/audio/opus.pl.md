{
  "date" : "2021-02-26",
  "keywords" :["OPUS", "plik", "rozszerzenie", "format", "Kodowanie dźwięku"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików OPUS i interfejsy API, które mogą tworzyć i otwierać pliki OPUS.",
  "title" :"OPUS",
  "linktitle" : "OPUS",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-26"
}

## Czym jest plik OPUS?

Opus to format pliku audio stworzony przez fundację Xiph.Org, a później standaryzowany przez IETF (Internet Engineering Task Force). Został opracowany głównie do przesyłania strumieniowego w Internecie, Voice over IP (VOIP), wideokonferencji i czatu w grze, dlatego został zaprojektowany tak, aby zachować niskie opóźnienia przy zachowaniu interaktywnej komunikacji w czasie rzeczywistym. Zachowując jakość dźwięku pliku Opus, wiele ślepych testów odsłuchowych wykazało, że Opus jest formatem audio wysokiej jakości niż jakikolwiek inny format audio przy danej przepływności.

## Specyfikacje formatu plików OPUS

Format Opus wykorzystuje zarówno kodeki SILK (używane przez Skype), jak i Xiph.Org i obsługuje zmienne przepływności od 6 kb/s do 510 kb/s. Rozszerzenie Opus wykorzystuje zorientowany na mowę algorytm SILK oparty na LPC i algorytm CELT oparty na MDCT o niższym opóźnieniu, czasami przełączając się między obydwoma lub czasami łącząc oba algorytmy, aby zapewnić maksymalną wydajność. Pliki w formacie Opus mają rozszerzenie .opus. W przeciwieństwie do formatu pliku Vorbis, Opus nie wymaga dużych książek kodowych dla każdego pojedynczego pliku, dlatego ten format jest stosunkowo wydajny.

## Bibliografia ##

* [OPUS – z Wikipedii](https://en.wikipedia.org/wiki/Opus_(audio_format))

