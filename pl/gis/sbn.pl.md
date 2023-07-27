{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - plik binarny indeksu przestrzennego ESRI",
  "description":"Dowiedz się o formacie pliku SBN i interfejsach API, które mogą tworzyć i otwierać pliki SBN.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Czym jest plik SBN?

Plik z rozszerzeniem .sbn jest plikiem indeksu przestrzennego, który jest powiązany z plikiem ESRI ArcGIS [.shp](/pl/gis/shp/). Służy do optymalizacji zapytań przestrzennych po przeprowadzeniu indeksowania danych. Innym typem pliku używanym obok .sbn jest plik .sbx. Pliki SBN i SBX razem tworzą indeks kształtu, aby przyspieszyć zapytania przestrzenne. Pliki SBN są opcjonalne i można je otwierać za pomocą [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## Format pliku SBN — więcej informacji

Pliki SBN są zapisywane na dysku jako pliki binarne, a szczegóły ich wewnętrznego formatu nie są dostępne. Przechowują one binarną reprezentację pliku SHP dla zapytań przestrzennych. Plik indeksu SBX jest używany wraz z plikami SBN do przyspieszenia zapytań przestrzennych w plikach kształtu.

## Bibliografia

* [Opis techniczny ESRI ShapeFile](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

