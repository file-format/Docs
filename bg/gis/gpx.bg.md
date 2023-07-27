{
  "date" : "2019-10-11",
  "keywords" :[ "gpx файл", "какво е gpx файл", "файл", "gpx пример", "gpx файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX – файлов формат за обмен на GPX",
  "description":"Научете за GPX файловия формат и API, които могат да създават и отварят GPX файлове.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е GPX файл?

Файловете с разширение GPX представляват GPS Exchange формат за обмен на GPS данни между приложения и уеб услуги в интернет. Това е лек XML файлов формат, който съдържа GPS данни, т.е. точки, маршрути и следи, които да бъдат импортирани и червени от множество програми. Файловият формат GPX е отворен и се поддържа от различни приложения и GPS устройства. GPS данни от такива файлове могат да бъдат заредени за показване в приложения за картографиране за геопространствени цели.

## GPX файлов формат ##

GPX файлът се състои от данни за географска ширина и дължина, стойности на надморска височина и друга вероятно друга описателна информация. Данните за местоположението се изразяват като десетични градуси, а надморската височина се изразява в метри. Времето в GPX файл е в координирано универсално време (UTC), използвайки формат ISO 8601. Ползите от използването на GPX файл са следните:

* GPX ви позволява да обменяте данни с нарастващ списък от програми за Windows, MacOS, Linux, Palm и PocketPC.
* GPX може да се трансформира в други файлови формати с помощта на проста уеб страница или програма за конвертиране.
* GPX е базиран на XML стандарта, така че много от новите програми, които използвате (например Microsoft Excel), могат да четат GPX файлове.
* GPX улеснява всеки в мрежата да разработва нови функции, които незабавно ще работят с любимите ви програми.

[GPX схемата](https://www.topografix.com/GPX/1/1/gpx.xsd) показва представянето на файловия формат GPX за справка.

### Основни данни ###

Следват основни данни, които са част от GPX файл за представяне на GPS данни.

* **Пътни точки**: Пътната точка е WGS84 (GPS) координати на точка и представлява слой от характеристики от OGR тип wkbPoint
* **Маршрути**: Представлява слой от функции от OGR тип wkbLineString. Той включва списък с точки от следите, които са точки от пътя, показващи завой или етапи, които водят до дестинация
* **Пътечки**: Следите представляват слой от функции от OGR тип wkbMultiLineString. Състои се от поне един сегмент, съдържащ точки в подреден списък от точки, описващи път. Състои се от списък с точки от трак, които представляват непрекъснат GPS трак.

### GPX примерен файл ###

Следният GPX файл показва организацията на GPS данни в GPX файл и може да даде добра представа за съдържанието на GPX файл.

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

## Препратки ##

* [GPX файлов формат](https://www.topografix.com/gpx.asp)
* [GPX – от Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

