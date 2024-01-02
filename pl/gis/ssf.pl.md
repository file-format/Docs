{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - plik standardowego formatu przechowywania Trimble",
  "description":"Poznaj format plików SSF i interfejsy API, które mogą tworzyć i otwierać pliki SSF.",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## Czym jest plik SSF?

Plik z rozszerzeniem .ssf to format pliku do przechowywania danych geoprzestrzennych używany przez aplikacje nawigacyjne GIS firmy [Trimble](https://www.trimble.com). Przechowuje dane GPS zarejestrowane w terenie za pomocą urządzeń Trimble. Dziennik GPS jest następnie importowany do jednej z aplikacji pakietu aplikacji Trimble. Dziennik GPS zawarty w SSF służy do tworzenia niestandardowych układów współrzędnych. Pliki SSF można otwierać za pomocą [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/en/products/software/office-software), Trimble Navigation GPS Pathfinder Tools SDK i ESRI ArcGIS for Desktop z Wtyczka Trimble GPS Analyst.

## Format pliku SSF — więcej informacji

Gdy dane GPS są przesyłane z urządzenia Trimble do komputera w celu dalszego przetwarzania, wszystkie te pliki są łączone w jeden plik .ssf. Ten surowy nieprzetworzony plik jest używany przez oprogramowanie do przetwarzania końcowego do wprowadzania poprawek i pomocy w zarządzaniu danymi.

Pliki SSF są zapisywane na dysku w zastrzeżonym formacie plików firmy Trimble, a ich szczegółowe specyfikacje nie są dostępne publicznie. Jest specyficzny dla urządzeń Trimble i reprezentuje dane jednostki GPS. Do tej pory nie jest dostępne żadne niekomercyjne bezpłatne rozwiązanie do odczytu lub konwersji plików SSF.

## Bibliografia

* [Informacja prasowa Trimble](https://www.trimble.com/news/release.aspx?id=050510b)

