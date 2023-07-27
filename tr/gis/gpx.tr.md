{
  "date" : "2019-10-11",
  "keywords" :[ "gpx dosyası", "gpx dosyası nedir", "dosya", "gpx örneği", "gpx dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Değişim Dosyası Formatı",
  "description":"GPX dosya formatı ve GPX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## GPX dosyası nedir?

GPX uzantılı dosyalar, GPS verilerinin internetteki uygulamalar ve web hizmetleri arasında değiş tokuşu için GPS Değişim formatını temsil eder. Bu, birden fazla program tarafından içe aktarılacak ve kırmızı olacak GPS verilerini, yani ara noktaları, rotaları ve izleri içeren hafif bir XML dosya formatıdır. GPX dosya formatı açıktır ve çeşitli uygulamalar ve GPS cihazları tarafından desteklenir. Bu tür dosyalardan alınan GPS verileri, jeo-uzaysal amaçlarla haritalama uygulamalarında görüntülenmek üzere yüklenebilir.

## GPX Dosya Biçimi ##

Bir GPX dosyası, enlem ve boylam konum verilerinden, yükseklik değerlerinden ve diğer olası tanımlayıcı bilgilerden oluşur. Konum verileri ondalık derece olarak ifade edilir ve yükseklik metre olarak ifade edilir. Bir GPX dosyasındaki saat, ISO 8601 formatı kullanılarak Eşgüdümlü Evrensel Saat (UTC) cinsindendir. Bir GPX dosyası kullanmanın faydaları şunlardır:

* GPX, Windows, MacOS, Linux, Palm ve PocketPC için sayıları giderek artan programlarla veri alışverişi yapmanızı sağlar.
* GPX, basit bir web sayfası veya dönüştürücü programı kullanılarak diğer dosya biçimlerine dönüştürülebilir.
* GPX, XML standardını temel alır, dolayısıyla kullandığınız yeni programların çoğu (örneğin Microsoft Excel) GPX dosyalarını okuyabilir.
* GPX, web'deki herkesin en sevdiğiniz programlarla anında çalışacak yeni özellikler geliştirmesini kolaylaştırır.

[GPX Şeması](https://www.topografix.com/GPX/1/1/gpx.xsd), referans için GPX dosya formatının gösterimini gösterir.

### Temel Veriler ###

Aşağıda, GPS verilerinin temsili için bir GPX dosyasının parçası olan temel veriler yer almaktadır.

* **Yol Noktaları**: Yol noktası, bir noktanın WGS84 (GPS) koordinatlarıdır ve OGR türü wkbPoint'in özellikler katmanını temsil eder.
* **Yollar**: OGR tipi wkbLineString'in bir özellik katmanını temsil eder. Bir dönüşü gösteren yol noktaları veya bir varış noktasına götüren aşama noktaları olan izleme noktalarının bir listesini içerir.
* **İzler**: İzler, OGR tipi wkbMultiLineString'in özellik katmanını temsil eder. Bir yolu tanımlayan sıralı bir noktalar listesinde ara noktaları içeren en az bir parçadan yapılır. Sürekli bir GPS izini temsil eden bir iz noktaları listesinden oluşur.

### GPX Örnek Dosyası ###

Aşağıdaki GPX dosyası, bir GPX dosyasındaki GPS verilerinin organizasyonunu gösterir ve bir GPX dosyasının içeriği hakkında iyi bir fikir verebilir.

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

## Referanslar ##

* [GPX Dosya Biçimi](https://www.topografix.com/gpx.asp)
* [GPX - Wikipedia Tarafından](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

