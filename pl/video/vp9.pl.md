{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Plik", "Rozszerzenie", "Format pliku", "Format wideo", "Wideo TrueMotion", "VPX", "Technologie On2"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 — plik wideo TrueMotion",
  "description":"Poznaj format plików VP9 i interfejsy API, które mogą tworzyć i otwierać pliki VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Czym jest plik VP9?

Firma Google opracowała kodek VP9 jako nieodpłatny standard kodowania wideo typu open source jako następca VP8. Pierwotnie został zaprojektowany do kompresji treści Ultra HD na YouTube, ponieważ rozszerza i zwiększa wydajność kodowania swojego poprzednika. Jeśli mówimy o oryginalnych kodekach VPX, pochodziły one z On2 Technologies, które zostało zasymilowane przez Google w 2010 roku. Google później udostępnił kodek jako open source. Oba formaty VP8 i VP9 są dostępne w ramach bezpłatnej licencji BSD, która umożliwia operatorom organizowanie biegłości w kodowaniu lub dekodowaniu zarówno w ekskluzywnym oprogramowaniu, jak i oprogramowaniu typu open source bez ujawniania kodu źródłowego.

## Cechy techniczne VP9

* VP9 zapewnia maksymalną rozdzielczość 8192x4352 przy 120 fps i wielu przestrzeniach kolorów, z Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 i sRGB
* Pełen zakres zastosowań internetowych i mobilnych, od kompresji o niskiej przepływności po wysokiej jakości ultra-HD, z dodatkową obsługą kodowania 10/12-bitowego i HDR, jest w pełni obsługiwany przez ten format
* Może zmniejszyć szybkość transmisji wideo nawet o 50% w porównaniu z innymi
* Jest przygotowany do adaptacyjnego przesyłania strumieniowego i jest używany przez YouTube i innych znanych dostawców internetowych filmów wideo
* Urządzenia Chrome, Opera, Edge, Firefox i Android, a także miliony inteligentnych telewizorów obsługują dekodowanie tego kodeka
* Rozdzielczości wideo większe niż 1080p są modyfikowane przez VP9 i umożliwiają bezstratną kompresję
* Różne przestrzenie kolorów, takie jak Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 i sRGB są obsługiwane przez VP9
* Wideo HDR przy użyciu Hybrid Log-Gamma i Perceptual Quantizer może być również obsługiwane przez VP9


## Krótka historia

* Rozwój kodeka wideo VP9 rozpoczął się w 2011 roku, a jego dekoder został dodany do przeglądarki internetowej Chromium w grudniu 2012 roku
* Jego pierwsza wersja przeglądarki internetowej Google Chrome została wydana w lutym 2013 r. I wtedy wydano dekodowanie
* Google udostępnił Chrome 29.0.1547 z ostateczną obsługą VP9 w sierpniu 2013 r
* W październiku 2013 do FFmpeg dodano instynktowny dekoder VP9
* Mozilla dodała wsparcie VP9 do Firefoksa w grudniu 2013 w wersji 2, która została wydana 18 marca 2014
 

## Działanie VP9

Zwykle wideo 4K podnosi jakość obrazu, zmniejszając określone piksele, a kodek VP9 i HEVC zwiększają je, aby zmniejszyć szybkość transmisji i rozmiar pliku. Chociaż może się to wydawać sprzeczne, silnik kodowania bierze większe piksele i przekształca je w produkt o lepszej rozdzielczości. Źródłowe wideo, obejmujące klatki wideo, jest kodowane lub kompresowane w celu utworzenia skompresowanego strumienia bitów wideo. Każda oddzielna klatka jest najpierw dzielona na bloki pikseli. Bloki są następnie analizowane pod kątem trójwymiarowych odrzuceń, a sekwencyjne połączenia między ramkami są oceniane pod kątem wykorzystania obszarów, których nie można zmienić. Są one kodowane za pomocą wektorów ruchu, które zapewniają jakość danego bloku w następnej klatce. Informacje szczątkowe są kodowane przy użyciu efektywnej kompresji binarnej.

## Bibliografia

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [Dokumenty internetowe MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Kokos](https://www.coconut.co/)

