{
  "date" : "2019-10-11",
  "keywords" :["plik qlr", "format pliku qlr", "co to jest plik qlr", "plik", "przykład qlr", "rozszerzenie pliku qlr", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - plik definicji warstwy QGIS",
  "description":"Poznaj format plików QLR i interfejsy API, które mogą tworzyć i otwierać pliki QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Czym jest plik QRL?

Plik z rozszerzeniem .qlr to plik definicji warstwy zawierający wskaźnik do źródła danych warstwy. Jest to dodatek do informacji o stylu [QGIS](https://www.qgis.org/en/site/) dla warstwy. Mając odniesienia do wszystkich powiązanych stylów, ten plik jest używany jako pojedyncze źródło danych, które mają być użyte do uzyskania informacji o stylach. Korzystając z plików QLR, informacje do źródeł danych można umieścić w tym pojedynczym pliku, który może być odczytywany przez inne aplikacje w celu załadowania informacji o stylizacji. Pliki QLR można otwierać za pomocą dowolnego edytora tekstu, takiego jak Notepad ++.

## Format pliku QLR

QLR, podobnie jak [QGS](/pl/gis/qgs/), jest plikiem XML zawierającym wskaźniki do źródła danych warstwy w postaci znaczników XML. Jest podobny do pliku ArcGIS .lyr. Tagi najwyższego poziomu pliku QML są pokazane na poniższym obrazku.

{{< figure src="../qlr.png" title="" >}}

## Bibliografia

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

