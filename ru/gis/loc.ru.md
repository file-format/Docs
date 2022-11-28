{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "файл", "расширение", "формат файла", "Местоположение GPS", "Путевая точка" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - формат файла местоположения GPS",
  "description":"Узнайте о формате файла LOC и API-интерфейсах, которые могут создавать и открывать файлы LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## .LOC вариант №

Файл с расширением .loc представляет собой файл местоположения GPS, который содержит геопространственные местоположения в качестве путевых точек. Путевая точка — это пара значений широта-долгота, которая относится к местоположению, используемому приложениями географической информационной системы (ГИС). Картографические программы GPS, такие как DeLorme Topo, используют файлы LOC для чтения и отображения информации, содержащейся в этих файлах LOC, в виде выбираемых конечными пользователями слоев. Кроме того, они используются для обмена данными GPS между приложениями. Файлы LOC можно открывать с помощью таких приложений, как [TopoGrafix EasyGPS] (https://www.easygps.com/), которые отображают содержимое таких файлов в виде слоев и данных, нанесенных на карту в соответствующем географическом положении.

## Формат файла LOC — дополнительная информация

Файлы LOC похожи на файлы [GPX](/ru/gis/gpx/), но сохраняются в другом формате. Они сохраняются в виде файлов [XML](/ru/web/xml/), в которых содержимое путевых точек и связанная с ними информация содержится в структурированных тегах. Поскольку XML является обобщенным языком для обмена данными между различными приложениями, это облегчает обмен данными LOC с другими приложениями.

## Формат файла LOC — пример

Ниже приведены заголовок и текст одной путевой точки из файла LOC. Как видно, информация заголовка содержит источник местоположения данных. Путевая точка содержит такую информацию, как «ID» и соответствующие данные содержимого, связанные с путевой точкой. Наконец, путевая точка представляет собой набор значений широты и долготы, а также текст, связанный с этой конкретной путевой точкой.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## использованная литература

* [TopGraphic EasyGPS] (https://www.easygps.com/)
