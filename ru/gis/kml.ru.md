{
  "date" : "2019-10-11",
  "keywords" :[ "файл kml", "что такое файл kml", "файл", "пример kml", "расширение файла kml", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML — язык разметки замочной скважины",
  "description":"Узнайте о формате файлов KML и API, которые могут создавать и открывать файлы KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .KML вариант №

KML, язык разметки Keyhole) содержит геопространственную информацию в нотации XML. Файлы, сохраненные в формате KML, можно открывать в приложениях географической информационной системы (ГИС) при условии, что они это поддерживают. Многие приложения начали поддерживать формат файлов KML после того, как он был принят в качестве международного стандарта. KML использует структуру на основе тегов с вложенными элементами и атрибутами. Все теги чувствительны к регистру, и важно соблюдать порядок этих тегов в соответствии со справочником [KML](https://developers.google.com/kml/documentation/kmlreference).

## Краткая история ##

KML изначально был разработан для использования с Google Планета Земля, который первоначально был известен как Keyhole Earth Viewer. KLM был принят в качестве международного стандарта в 2008 году Открытым геопространственным консорциумом в 2008 году. Поскольку этот формат был разработан для использования с Google Планета Земля, он стал первым, кто просматривает и редактирует файлы KML. С течением времени появляется все больше и больше проектов, которые обеспечивают поддержку форматов файлов KML, включая несколько API на разных языках.

## Спецификации формата файлов KML ##

Справочник по KML — это полное руководство по использованию полных спецификаций форматов файлов. Стандартный файл KML состоит из:

* Метки
* Описательный HTML в метках
* Наземные накладки
* Пути
* Полигоны

В дополнение к этому расширенная версия файла KML может содержать:

* Стили для геометрии
* Стили для выделенных значков
* Наложения на экран
* Сетевые ссылки

Каждый элемент KML содержит информацию о широте и долготе, которая определяет географическое положение информации, присутствующей в файле. Однако могут быть и дополнительные параметры, такие как курс, высота и наклон.

### Метки места ###

Он используется для обозначения положения на поверхности Земли и определяется<Point> элемент. Ниже приведен пример представления метки в файле KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Описательный HTML в метках ###

С меткой может быть связана дополнительная информация, которая дополнительно улучшает представление метки. Такая информация включает ссылки, размеры шрифта, стили и цвета. Кроме того, он также включает выравнивание текста и таблицы, которые должны быть частью метки.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Наложения на землю ###

Они представляют собой наложение изображения на поверхность Земли.<icon> Элемент содержит ссылку на файл изображения оверлея.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Пути ###

Пути представлены<LineString> элемент, представляющий собой набор пар широта-долгота. Используя их, в Google Планета Земля можно создать множество различных типов путей.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Пространственная привязка в файле KML ##

Информация, содержащаяся в любом геопространственном файле о географических местоположениях, может иметь различное значение без информации о пространственной привязке. По умолчанию пространственная привязка файла KML определяется Всемирной геодезической системой 1984 года, WGS84.

## Использованная литература ##

* [Справочник по KML](https://developers.google.com/kml/documentation/kmlreference)
* [Учебник Google для разработчиков по KML](https://developers.google.com/kml/documentation/kml_tut)
* [Формат файла KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

