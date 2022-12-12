{
  "date" : "2019-10-11",
  "keywords" :[ "kml файл", "какво е kml файл", "файл", "kml пример", "kml файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML – Keyhole Markup Language",
  "description":"Научете за файловия формат KML и API, които могат да създават и отварят KML файлове.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е KML файл?

KML, Keyhole Markup Language) съдържа геопространствена информация в XML нотация. Файловете, записани като KML, могат да се отварят в приложения за географска информационна система (GIS), при условие че го поддържат. Много приложения започнаха да предоставят поддръжка за файловия формат KML, след като той беше приет като международен стандарт. KML използва базирана на тагове структура с вложени елементи и атрибути. Всички тагове са чувствителни към малки и големи букви и редът на тези тагове, съгласно [KML](https://developers.google.com/kml/documentation/kmlreference) справочника, е важно да се следва.

## Кратка история ##

KML първоначално е разработен за използване с Google Earth, който първоначално е известен като Keyhole Earth Viewer. KLM беше приет като международен стандарт през 2008 г. от Open Geospatial Consortium през 2008 г. Тъй като форматът е разработен за използване с Google Earth, той има отличието да бъде първият, който преглежда и редактира KML файлове. С течение на времето вече има все повече проекти, които осигуряват поддръжка за KML файлови формати, включително няколко API на различни езици.

## Спецификации на KML файлов формат ##

KML Reference е пълно ръководство за препращане, за да имате пълните спецификации на файловия формат. Стандартният KML файл се състои от:

* Маркери
* Описателни HTML в маркери
* Земни наслагвания
* Пътеки
* Многоъгълници

В допълнение към тях, разширена версия на KML файл може да има:

* Стилове за геометрия
* Стилове за подчертани икони
* Екранни наслагвания
* Мрежови връзки

Всеки KML елемент има lat-long информация, която локализира информацията във файла. Въпреки това, може да има допълнителни параметри, както и посока, надморска височина и наклон.

### Маркери ###

Използва се за представяне на позиция на земната повърхност и се идентифицира от<Point> елемент. Следва пример как е представен маркер на място в KML файл.

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

### Описателен HTML в показалци ###

Допълнителна информация може да бъде свързана с показалец, който допълнително подобрява представянето на показалеца. Тази информация включва връзки, размери на шрифта, стилове и цветове. Освен това включва подравняване на текст и таблици, които да бъдат част от показалеца.

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

### Наземни наслагвания ###

Те представляват наслояване на изображение върху повърхността на Земята. The<icon> elment съдържа връзката към файла с насложено изображение.

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

### Пътища ###

Пътищата са представени от<LineString> елемент, който е колекция от двойки lat-long. Използвайки ги, в Google Земя могат да бъдат създадени много различни типове пътища.

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

## Пространствено препращане в KML файл ##

Информацията, съдържаща се във всеки геопространствен файл за геолокации, може да има различни значения без информация за пространствена препратка. По подразбиране пространственото препращане на KML файл се определя от Световната геодезическа система от 1984 г., WGS84.

## Препратки ##

* [KML справка](https://developers.google.com/kml/documentation/kmlreference)
* [Урок за разработчици на Google за KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML файлов формат](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

