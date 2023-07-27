{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku WMV",
  "description":"Poznaj format pliku WMV i interfejsy API, które mogą tworzyć i otwierać pliki WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Co to jest plik WMV?

Advanced Systems Format (ASF) to cyfrowy kontener multimedialny przeznaczony głównie do przechowywania i przesyłania strumieni multimedialnych. Microsoft Windows Media Video (WMV) to skompresowany format wideo, a Microsoft Windows Media Audio (WMA) to skompresowany format audio wraz z dodatkowymi metadanymi w kontenerze ASF opracowanym przez firmę Microsoft. Po zakodowaniu plików WMV lub WMA za pomocą kodeków Windows Media Video i Windows Media Audio są one reprezentowane z rozszerzeniem .asf. WMV kompresuje duże pliki w celu uzyskania lepszej szybkości transmisji w sieci przy jednoczesnym zachowaniu jakości wideo. WMV jest specjalnie zaprojektowany do działania na wszystkich urządzeniach z systemem Windows. Po standaryzacji przez Stowarzyszenie Inżynierów Filmowych i Telewizyjnych (SMPTE), WMV jest obecnie uważany za format o otwartym standardzie.

## Historia ##

Przy pomocy zastrzeżonych kodeków Microsoftu w 1999 roku został opracowany nowy skompresowany format wideo znany jako WMV7, który był oparty na MPEG-4 Part 2. Ulepszenia zostały dodane w kolejnych dwóch wersjach, tj. WMV8 i 9. Microsoft przedstawił dziewiątą wersję WMV do SMPTE w celu standaryzacji w 2003 r., który ostatecznie został znormalizowany w 2006 r. jako SMPTE 421M, znany również jako VC-1. Ideą WMV było opracowanie formatu multimediów, który mógłby być obsługiwany przez cały sprzęt i oprogramowanie obsługiwane przez firmę Microsoft. Ponadto innym ważnym celem było przesyłanie strumieni wideo przez Internet w optymalnym scenariuszu. Po standaryzacji z SMPTE, WMV stał się również formatem wideo dla dysków Blu-ray.

## Specyfikacje formatu plików

### Pojemnik

Ogólnie rzecz biorąc, WMV jest pakowany do kontenera ASF, ale dodatkowo kontener Matroska lub AVI może również obsługiwać go z rozszerzeniami odpowiednio .mkv i .avi.

### Windows Media Video 9

Chociaż w serii Windows Media Video 9 dostępne są różne kodeki audio i wideo do tworzenia i odtwarzania multimediów cyfrowych, kodek WMV-9 jest najnowszym i najlepszym kodekiem wideo, ponieważ umożliwia uzyskanie optymalnej kompresji przy bardzo niskich przepływnościach, tj. 120 przy 10 Kb/s do 1920 x 1080 przy 4-8 Mb/s dla różnych filmów HD.

### Struktura kodeka

WMV-9 ma 8-bitowy wewnętrzny format kolorów 4:2:0. Podobnie jak wszystkie inne popularne standardy kompresji wideo MPEG-1 i H.261, WMV-9 wykorzystuje schemat blokowej kompensacji ruchu i transformacji przestrzennej. Ogólnie można powiedzieć, że te standardy wykonują blok po bloku kompensację ruchu z poprzedniej zrekonstruowanej klatki za pomocą wielkości 2-D zwanej wektorem ruchu (MV) w celu zasygnalizowania przemieszczenia przestrzennego. Bieżący blok jest tworzony za pomocą przewidywania wartości z poprzednio zrekonstruowanej klatki o tym samym rozmiarze, która jest przesunięta z aktualnej pozycji o wektor ruchu. Ostatecznie błąd resztkowy jest obliczany jako różnica między blokiem przewidywanym z kompensacją ruchu a blokiem rzeczywistym. Ten błąd resztkowy jest przekształcany za pomocą liniowej transformacji zagęszczającej energię, a następnie skwantyzowany i kodowany entropijnie.

Kwantyzowane współczynniki przekształcenia są dekodowane entropijnie, dekwantowane i przekształcane odwrotnie w celu uzyskania przybliżenia błędu resztkowego po stronie dekodera, który jest następnie dodawany do predykcji z kompensacją ruchu w celu wygenerowania rekonstrukcji. Opis wysokiego poziomu kodera-dekodera pokazano na poniższej ilustracji.

W dalszej części tej sekcji zostaną omówione nowe ulepszenia WMV-9, które odróżniają go od pozostałych rozwiązań do kodowania wideo, takich jak standardy MPEG. WMV-9 ma ramki intra (I), przewidywane (P) i przewidywane dwukierunkowo (B). Ramki wewnętrzne to te, które są kodowane niezależnie i nie są zależne od innych ramek. Klatki przewidywane to klatki, które zależą od jednej klatki z przeszłości. Dekodowanie przewidywanej ramki może nastąpić dopiero po zdekodowaniu wszystkich ramek odniesienia poprzedzających bieżącą ramkę, począwszy od ostatniej (I) ramki. Klatki B to klatki, które mają dwa odniesienia — jedno w czasowej przeszłości i jedno w czasowej przyszłości. Ramki B są przesyłane po ich odniesieniach, co oznacza, że ramki B są wysyłane poza kolejnością, aby zapewnić dostępność ich odniesień w czasie dekodowania. Ramki B w WMV-9 nie są używane jako odniesienie dla kolejnych ramek. Powoduje to umieszczenie ramek B poza pętlą dekodowania, umożliwiając korzystanie ze skrótów podczas dekodowania ramek B bez dryfu lub długotrwałych artefaktów wizualnych. Powyższa definicja ramek I, P i B odnosi się zarówno do sekwencji progresywnych, jak i z przeplotem.

Wydajność kodeków wideo jest porównywana z wykresem wskaźnika zniekształceń (RD). Jest to krzywa 2-D, która pokazuje zniekształcenia powstałe w wyniku kompresji przy określonej przepływności.

WMV-9 rozwiązał ten problem, wprowadzając różne techniki wymienione poniżej:

1. Adaptacyjna transformacja rozmiaru bloku

2. Zestaw transformacji o ograniczonej precyzji

3. Kompensacja ruchu

4. Kwantyzacja i dekwantyzacja

5. Zaawansowane kodowanie entropijne

6. Filtrowanie pętli

7. Zaawansowane kodowanie ramek B

8. Kodowanie z przeplotem

9. Wygładzanie zakładek

10. Narzędzia niskobudżetowe

11. Kompensacja zanikania

## Bibliografia ##

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html)
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


