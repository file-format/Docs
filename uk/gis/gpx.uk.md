{
  "date" : "2019-10-11",
  "keywords" :[ "файл gpx", "що таке файл gpx", "файл", "приклад gpx", "розширення файлу gpx", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - формат файлу обміну GPX",
  "description":"Дізнайтеся про формат файлу GPX та API, які можуть створювати та відкривати файли GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл GPX?

Файли з розширенням GPX представляють формат GPS Exchange для обміну даними GPS між програмами та веб-сервісами в Інтернеті. Це легкий формат XML-файлу, який містить дані GPS, тобто маршрутні точки, маршрути та треки, які потрібно імпортувати та відображати кількома програмами. Формат файлу GPX є відкритим і підтримується різними програмами та пристроями GPS. Дані GPS із таких файлів можна завантажити для відображення в програмах картографування для геопросторових цілей.

## Формат файлу GPX ##

Файл GPX містить дані про широту та довготу, значення висоти та іншу, можливо, іншу описову інформацію. Дані про місцезнаходження виражаються в десяткових градусах, а висота виражається в метрах. Час у файлі GPX указано за всесвітнім координованим часом (UTC) у форматі ISO 8601. Переваги використання файлу GPX такі:

* GPX дозволяє обмінюватися даними з дедалі більшим списком програм для Windows, MacOS, Linux, Palm і PocketPC.
* GPX можна перетворити в інші формати файлів за допомогою простої веб-сторінки або програми-конвертера.
* GPX базується на стандарті XML, тому багато нових програм, які ви використовуєте (наприклад, Microsoft Excel), можуть читати файли GPX.
* GPX дозволяє будь-кому в Інтернеті легко розробляти нові функції, які миттєво працюватимуть із вашими улюбленими програмами.

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) показує представлення формату файлу GPX для довідки.

### Основні дані ###

Нижче наведено важливі дані, які є частиною файлу GPX для представлення даних GPS.

* **Шляхові точки**: маршрутна точка – це координати WGS84 (GPS) точки та представляють шар об’єктів типу OGR wkbPoint
* **Маршрути**: представляють рівень функцій OGR типу wkbLineString. Він містить список точок маршруту, які є точками маршруту, що показують повороти або точки етапу, які ведуть до пункту призначення
* **Доріжки**: Доріжки представляють шар функцій OGR типу wkbMultiLineString. Він складається принаймні з одного сегмента, що містить маршрутні точки в упорядкованому списку точок, що описують шлях. Він складається зі списку точок треку, які представляють безперервний трек GPS.

### Файл прикладу GPX ###

Наступний файл GPX показує організацію даних GPS у файлі GPX і може дати гарне уявлення про вміст файлу GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Посилання ##

* [Формат файлу GPX](https://www.topografix.com/gpx.asp)
* [GPX – Вікіпедія](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

