{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku CPG - plik strony kodowej ESRI",
  "description":"Dowiedz się o formacie pliku CPG i interfejsach API, które mogą tworzyć i otwierać pliki CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Czym jest plik CPG?

Plik CPG jest opcjonalnym plikiem wymaganym ESRI Shapefile, który służy do określenia strony kodowej do identyfikacji używanego zestawu znaków. Są one przechowywane w formacie zwykłego pliku tekstowego i zawierają informacje o kodowaniu zastosowanym do utworzenia pliku kształtu. W przypadku, gdy plik CPG nie jest dostępny, plik kształtu używa domyślnego kodowania systemowego. Plik CPG, jeśli istnieje, musi mieć taki sam przedrostek jak plik [SHP](/pl/gis/shp/), na przykład roads.shp, roads.cpg.

Pliki CPG można otwierać za pomocą ESRI ArcGIS Pro.

### Format pliku CPG — więcej informacji

Podczas przeglądania pliku kształtu w ArcCatalog lub dowolnej innej aplikacji ArcGIS widoczny jest tylko plik kształtu. Ale w rzeczywistości plik kształtu używa innych powiązanych plików, które są odczytywane razem z głównym plikiem kształtu. Plik CPG jest również jednym z nich, jeśli jest obecny obok głównego pliku SHP.

## Bibliografia

* [Rozszerzenia plików Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

