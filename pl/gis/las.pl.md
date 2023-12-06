{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Format pliku Lidar LAser",
  "description":"Dowiedz się o formacie pliku LAS i interfejsach API, które umożliwiają tworzenie i otwieranie plików LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Czym jest plik LAS?

Format pliku LAS (Lidar LASer) to format pliku binarnego zaprojektowany specjalnie do przechowywania danych chmury punktów lidar. Został opracowany i jest utrzymywany przez Amerykańskie Towarzystwo Fotogrametrii i Teledetekcji (ASPRS) jako ujednolicony format wymiany danych lidarowych i interoperacyjności.

Pliki LAS przechowują szczegółowe informacje o poszczególnych punktach lidarowych, w tym ich współrzędne 3D (x, y i z), wartości intensywności, kody klasyfikacyjne i dodatkowe atrybuty. Format obsługuje zarówno dane lidarowe o dyskretnym powrocie, jak i o pełnym kształcie fali, umożliwiając przechowywanie wielu zwrotów na impuls laserowy.

## Format pliku LAS

Struktura pliku LAS składa się z trzech głównych sekcji: nagłówka pliku, rekordów o zmiennej długości (VLR) i rekordów danych punktowych.

1. Nagłówek pliku: Nagłówek pliku zawiera podstawowe informacje o pliku LAS, takie jak wersja formatu danych, format danych punktów, liczba punktów, współrzędne ramki ograniczającej, system odniesienia za pomocą współrzędnych (CRS) i inne metadane. Zawiera podsumowanie danych lidarowych zawartych w pliku.

2. Rekordy o zmiennej długości (VLR): VLR są opcjonalne i mogą przechowywać dodatkowe metadane i niestandardowe informacje na temat danych lidarowych. VLR pozwalają na elastyczność w rozszerzaniu formatu w celu dostosowania do specyficznych wymagań użytkownika. Przykłady VLR obejmują informacje o systemie czujników, parametrach przetwarzania danych lub schematach klasyfikacji.

3. Rekordy danych punktowych: Rekordy danych punktowych przechowują rzeczywiste pomiary lidarowe. Każdy rekord danych punktowych reprezentuje pojedynczy punkt lidarowy i zawiera atrybuty, takie jak współrzędne x, y i z, wartości intensywności, kody klasyfikacyjne (np. grunt, roślinność, budynki) i inne atrybuty zdefiniowane przez użytkownika. W rekordach punktów można także przechowywać znaczniki czasu, liczniki zwrotów i kąty skanowania.

Pliki LAS obsługują różne formaty danych (od 0 do 10), aby pomieścić różne typy danych lidarowych i poziom potrzebnych informacji. Na przykład format 0 reprezentuje prosty format punktowy z podstawowymi informacjami, podczas gdy formaty 1 do 3 zapewniają bardziej wszechstronne dane, w tym informacje o przebiegu dla każdego powrotu.

Pliki LAS są szeroko obsługiwane przez oprogramowanie lidar i narzędzia do przetwarzania, co czyni je standardowym formatem wymiany i analizy danych lidarowych. Ponadto pliki LAS można kompresować przy użyciu technik kompresji bezstratnej w celu zmniejszenia rozmiaru pliku przy jednoczesnym zachowaniu wierności oryginalnych danych. Skompresowana wersja plików LAS jest często określana jako LAZ, która oferuje wydajne możliwości przechowywania i przesyłania danych.

## Bibliografia

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
