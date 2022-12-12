{
  "date" : "2019-10-11",
  "keywords" :[ "файл kml", "що таке файл kml", "файл", "приклад kml", "розширення файлу kml", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"Дізнайтеся про формат файлу KML та API, які можуть створювати та відкривати файли KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл KML?

KML, Keyhole Markup Language) містить геопросторову інформацію в нотації XML. Файли, збережені як KML, можна відкривати в програмах Географічної інформаційної системи (ГІС), якщо вони її підтримують. Багато програм почали підтримувати формат файлу KML після того, як він був прийнятий як міжнародний стандарт. KML використовує структуру на основі тегів із вкладеними елементами й атрибутами. Усі теги чутливі до регістру, і важливо дотримуватися порядку цих тегів відповідно до довідки [KML](https://developers.google.com/kml/documentation/kmlreference).

## Коротка історія ##

KML спочатку був розроблений для використання з Google Планета Земля, який спочатку був відомий як Keyhole Earth Viewer. KLM був прийнятий як міжнародний стандарт у 2008 році Відкритим геопросторовим консорціумом у 2008 році. Оскільки цей формат було розроблено для використання з Google Планета Земля, він має честь бути першим у форматі для перегляду та редагування файлів KML. З плином часу з’являється все більше проектів, які забезпечують підтримку форматів файлів KML, включаючи кілька API різними мовами.

## Специфікації формату файлу KML ##

Довідник KML є повним посібником для посилань, щоб мати повні специфікації формату файлу. Стандартний файл KML складається з:

* Мітки
* Описовий HTML у мітках місця
* Накладки на землю
* Шляхи
* Багатокутники

Окрім цього, розширена версія файлу KML може мати:

* Стилі для геометрії
* Стилі для виділених значків
* Накладання на екран
* Мережеві посилання

Кожен елемент KML містить інформацію про довжину, яка геолокує інформацію, наявну у файлі. Однак можуть бути додаткові параметри, а також напрямок, висота та нахил.

### Мітки ###

Він використовується для представлення положення на поверхні Землі та ідентифікується за допомогою<Point> елемент. Нижче наведено приклад того, як позначка місця представлена у файлі KML.

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

### Описовий HTML у мітках ###

Додаткова інформація може бути пов’язана з позначкою місця, що додатково покращує представлення позначки місця. Така інформація включає посилання, розміри шрифтів, стилі та кольори. Крім того, він також включає вирівнювання тексту та таблиці, які є частиною позначки місця.

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

### Накладки на землю ###

Вони являють собою нанесення зображення на поверхню Землі. The<icon> elment містить посилання на файл накладеного зображення.

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

### Шляхи ###

Шляхи представлені<LineString> елемент, який є набором пар lat-long. Використовуючи їх, у Google Планета Земля можна створити багато різних типів шляхів.

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

## Просторова прив’язка у файлі KML ##

Інформація, що міститься в будь-якому геопросторовому файлі про геолокації, може мати різне значення без просторової прив’язки. За замовчуванням просторове прив’язування файлу KML визначено Всесвітньою геодезичною системою 1984 року, WGS84.

## Посилання ##

* [Довідка KML](https://developers.google.com/kml/documentation/kmlreference)
* [Навчальний посібник розробника Google для KML](https://developers.google.com/kml/documentation/kml_tut)
* [Формат файлу KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

