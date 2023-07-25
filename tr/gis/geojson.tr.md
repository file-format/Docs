{
  "date" : "2019-10-11",
  "keywords" :[ "geojson dosyası", "geojson dosyası nedir", "dosya", "geojson örneği", "geojson dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - JSON tabanlı Coğrafi Dosya Formatı",
  "description":"GeoJSON dosya formatı ve GeoJSON dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## GeoJSON dosyası nedir?

GeoJSON, coğrafi özellikleri mekansal olmayan nitelikleriyle temsil etmek için tasarlanmış JSON tabanlı bir formattır. Bu format, farklı JSON (JavaScript Object Notation) nesnelerini ve bunların birleştirme şeklini tanımlar. JSON formatı, Coğrafi özellikler, bunların uzamsal kapsamları ve özellikleri hakkında toplu bir bilgiyi temsil eder. Bu dosyanın bir nesnesi, bir geometriyi (Nokta, ÇizgiDizesi, Çokgen), bir özelliği veya özellikler koleksiyonunu gösterebilir. Özellikler, adresleri ve yerleri sokaklar olarak, ana yollar ve sınırları çizgi dizileri olarak ve ülkeleri, iller ve kara bölgelerini çokgenler olarak yansıtır. GeoJSON kullanarak, farklı mobil yönlendirme ve navigasyon uygulamaları, hizmetlerinin kapsamını gösterebilir. GeoJSON'un bir uzantısı, boyutu daha küçük olan ve jeo-uzamsal topolojiyi kodlayan TopoJSON'dur.

## Kısa Tarih ##

İnternet Mühendisliği Görev Gücü (IETF), biçim yazarlarıyla birlikte GeoJSON'u Nisan 2015'te yayınlamak için bir [GeoJSON ÇG](https://datatracker.ietf.org/wg/geojson/charter/) oluşturdu. GeoJSON spesifikasyonu, [RFC 7946](https://tools.ietf.org/html/rfc7946), Ağustos 2016'da yayınlanan GeoJSON formatının yeni standart spesifikasyonu.

## GeoJSON Dosya Biçimi ##

### Koordinat ###

Koordinat, herhangi bir coğrafi verinin temel öğesidir. Bu, tek bir sayıyı (ondalık biçim) temsil eden tek bir boyuttur (Boylam, enlem) ve bazen yükseklik için bir koordinat da kaydeder. Zaman da bir boyut ama karmaşıklığı koordinat olarak kaydetmeyi zorlaştırıyor. Her iki JSON GeoJSON'daki koordinatlar sayılar gibi biçimlendirilmiştir.

### Durum ###

Sıralı bir koordinat dizisi [konumu](https://geojson.org/geojson-spec.html#positions) temsil eder. Bu, dünyadaki bir noktayı gösterebilen en küçük birimdir.

`[Boylam, enlem, yükseklik]`

Mevcut spesifikasyonun yayınlanmasından önce GeoJSON, konum başına üç koordinat kaydetmeye izin veriyordu ancak yeni spesifikasyon buna izin vermiyor.

### Geometri ###

Geometriler, GeoJSON'da bir tür ve bir koordinat koleksiyonundan oluşan basit şekillerdir (noktalar, eğriler ve yüzeyler). Nokta, tek bir konumu temsil eden en basit geometridir.

`{ "tip": "Nokta", "koordinatlar": [0, 0] }`

### Satır Dizileri ###

Bir çizgiyi temsil etmek için en az iki bağlantılı yer kullanılır.

`{ "type": "LineString", "koordinatlar": [[10, 30], [10, 10]] }`

Nokta ve çizgi dizileri, geometrinin en basit iki kategorisidir. Her iki geometri türü de pek çok geometrik kuralı rahatsız etmez. Bir nokta, herhangi bir yerde herhangi bir yerde temsil edilebilir ve bir çizgi, noktalar kendi kendini kesiyor olsa bile birden fazla noktaya sahip olabilir.

### Çokgenler ###

GeoJSON geometrileri, Çokgenlerde önemli ölçüde daha karmaşık görünmektedir. Çokgenlerin iç ve dış alanları vardır ve bu iç kısımlarda delikler olabilir.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

LineStrings ile karşılaştırıldığında, çokgenlerde, koordinat listesi iç içe geçmiş bir düzeydir ve çörek gibi kesiklere sahip olabilir.

### Koordinat Seviyesi ###

GeoJSON formatında, koordinat özelliği için dört derinlik seviyesi vardır.

### Özellikler ###

Geometriler, GeoJSON'un merkezi parçasıdır, bu nedenle gerçek dünya verileri, kimlik ve niteliklere sahip bu basit şekillerden daha fazlasıdır. Unsurlar, özelliklerini olduğu kadar geometriyi de kaydeder.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Özellik özellikleri, tek derinlikli anahtar değer eşlemeleri içeren bir tür [JSON](http://json.org/) nesnesi olabilir.

### Özellik Koleksiyonu ###

GeoJSON dosyalarının en üst seviyesinde, FeatureCollection şuna benzeyen en yaygın şeydir:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

GeoDjango, OpenLayers ve Geoforge yazılımı dahil olmak üzere birçok haritalama ve GIS yazılım paketi GeoJSON'u destekler. PostGIS ve Mapnik ile de uyumludur. Google, yahoo ve Bing haritalarının API hizmetleri de GeoJSON'u destekler.

## Referanslar ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Wikipedia Tarafından](https://en.wikipedia.org/wiki/GeoJSON)

