{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SBN - бінарний файл просторового індексу ESRI",
  "description":"Дізнайтеся про формат файлу SBN та API, які можуть створювати та відкривати файли SBN.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Що таке файл SBN?

Файл із розширенням .sbn — це файл просторового індексу, пов’язаний із файлом ESRI ArcGIS [.shp](/uk/gis/shp/). Він використовується для оптимізації просторових запитів, коли над даними виконано індексування. Інший тип файлу, який використовується поряд із .sbn, — це файл .sbx. Файли SBN і SBX разом складають індекс форми для прискорення просторових запитів. Файли SBN необов’язкові, їх можна відкрити за допомогою [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## Формат файлу SBN - Додаткова інформація

Файли SBN зберігаються на диску як двійкові файли, а деталі внутрішнього формату файлів недоступні. Вони зберігають двійкове представлення файлу SHP для просторових запитів. Файл індексу SBX використовується разом із файлами SBN для прискорення просторових запитів у шейп-файлах.

## Список літератури

* [Технічний опис ESRI ShapeFile](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)

