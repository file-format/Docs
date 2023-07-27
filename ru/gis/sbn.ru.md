{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN — двоичный файл пространственного индекса ESRI",
  "description":"Узнайте о формате файла SBN и API-интерфейсах, которые могут создавать и открывать файлы SBN.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## .SBN вариант №

Файл с расширением .sbn представляет собой файл пространственного индекса, связанный с файлом ESRI ArcGIS [.shp](/ru/gis/shp/). Он используется для оптимизации пространственных запросов, когда для данных был выполнен индекс. Другим типом файлов, используемым наряду с .sbn, является файл .sbx. Файлы SBN и SBX вместе составляют индекс формы для ускорения пространственных запросов. Файлы SBN являются необязательными и могут быть открыты с помощью [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## Формат файла SBN — дополнительная информация

Файлы SBN хранятся на диске в виде двоичных файлов, и сведения об их внутреннем формате файлов недоступны. В них хранится двоичное представление файла SHP для пространственных запросов. Файл индекса SBX используется вместе с файлами SBN для ускорения пространственных запросов к шейп-файлам.

## использованная литература

* [Техническое описание ESRI ShapeFile](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

