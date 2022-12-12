{
  "date" : "2019-10-11",
  "keywords" :["plik qml", "format pliku qml", "co to jest plik qml", "plik", "przykład qml", "rozszerzenie pliku qml", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML — format pliku w stylu QGIS",
  "description":"Poznaj format pliku QML i interfejsy API, które mogą tworzyć i otwierać pliki QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Czym jest plik QML?

Plik z rozszerzeniem .qml to plik XML przechowujący informacje o stylach warstw dla warstw QGIS. QGIS to wieloplatformowa aplikacja GIS typu open source służąca do wyświetlania danych geoprzestrzennych z możliwością organizowania danych w postaci warstw. Pliki QML zawierają informacje używane przez QGIS do renderowania geometrii obiektów, w tym definicje symboli, rozmiary i obroty, etykietowanie, krycie, tryb mieszania i wiele innych. W przeciwieństwie do plików QLR, pliki QML zawierają same w sobie wszystkie informacje o stylizacji. Pliki QML można otwierać w dowolnym edytorze tekstu, takim jak Notepad ++.

## Format pliku QML

QLR, podobnie jak [QGS](/pl/gis/qgs/) i [QLR](/pl/gis/qlr/), jest plikiem XML zawierającym informacje o stylach dla warstw.

Poniższy rysunek przedstawia znaczniki najwyższego poziomu pliku QML (z rozwiniętym tylko renderer_v2 i jego znacznikiem symbolu).

{{< figure src="../qml.png" title="" >}}

## Bibliografia

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

