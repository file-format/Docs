{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ – skompresowany plik wymiany danych LIDAR",
  "description":"Dowiedz się o formacie pliku LAZ i interfejsach API, które umożliwiają tworzenie i otwieranie plików LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Czym jest plik LAZ?

Format pliku LAZ to skompresowana wersja formatu pliku LAS (Lidar LASer), który został specjalnie zaprojektowany do przechowywania danych chmury punktów Lidar. Pliki LAZ zachowują te same dane i strukturę co pliki LAS, ale wykorzystują techniki kompresji bezstratnej w celu zmniejszenia rozmiaru pliku przy jednoczesnym zachowaniu oryginalnej wierności danych.

## Format pliku LAZ - krótka historia

Format pliku LAZ został opracowany w odpowiedzi na rosnące zapotrzebowanie na wydajne przechowywanie i przesyłanie dużych zbiorów danych lidarowych. Kompresując pliki LAS, pliki LAZ znacznie zmniejszają ich rozmiar, co ułatwia zarządzanie nimi i przesyłanie. Kompresję osiąga się poprzez zastosowanie kombinacji różnych algorytmów, takich jak kodowanie entropijne i kodowanie o zmiennej długości, w celu przedstawienia atrybutów punktu lidarowego w bardziej zwartej formie.

## Format pliku LAZ

Pomimo kompresji pliki LAZ zachowują możliwość pełnego przywrócenia oryginalnych danych LAS bez utraty informacji. Oznacza to, że po zdekompresowaniu pliku LAZ można go przetwarzać i analizować w taki sam sposób, jak nieskompresowany plik LAS. Proces kompresji i dekompresji jest zwykle przeprowadzany przy użyciu specjalistycznego oprogramowania lub bibliotek obsługujących format LAZ.

Format pliku LAZ zachowuje kompatybilność z plikami LAS, zapewniając interoperacyjność oprogramowania lidar i narzędzi do przetwarzania. Oznacza to, że aplikacje, które potrafią czytać i przetwarzać pliki LAS, zazwyczaj obsługują pliki LAZ bez żadnych modyfikacji. Ponadto pliki LAZ nadal zawierają nagłówek pliku, rekordy o zmiennej długości (VLR) i rekordy danych punktowych, zachowując tę samą strukturę co pliki LAS.

## Zalety formatu pliku LAZ

**Zmniejszony rozmiar pliku:** Kompresja LAZ znacznie zmniejsza rozmiar plików zbiorów danych lidarowych, czyniąc je łatwiejszymi w zarządzaniu oraz łatwiejszymi do przechowywania i przesyłania.

**Integralność danych:** Kompresja LAZ jest bezstratna, co oznacza, że zdekompresowane dane są dokładną repliką oryginalnych danych LAS, co gwarantuje brak utraty informacji i precyzji.

**Współpraca:** pliki LAZ są kompatybilne z plikami LAS, umożliwiając bezproblemową integrację z istniejącym oprogramowaniem lidar i przepływami pracy.

**Wydajne przetwarzanie:** Ze względu na zmniejszony rozmiar pliki LAZ można szybciej ładować i przetwarzać, co skraca ogólny czas przetwarzania i analizy.

Format pliku LAZ stał się powszechnie przyjęty w społeczności lidarów jako standard przechowywania i wymiany skompresowanych danych lidarowych. Zapewnia równowagę pomiędzy wydajną kompresją danych a integralnością danych, umożliwiając łatwiejszą obsługę dużych zbiorów danych lidarowych przy jednoczesnym zachowaniu dokładności i jakości oryginalnych danych.

## Bibliografia

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
