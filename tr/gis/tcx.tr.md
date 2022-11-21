{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX Dosya Formatı- Eğitim Merkezi XML Dosyası",
  "description":"TCX dosya formatı ve TCX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Bir TCX dosyası nedir?

TCX (Training Center XML) dosyası, fitness cihazları arasında veri paylaşmak için kullanılan bir veri alışverişi formatıdır. 2008 yılında Garmin'in Eğitim Merkezi ürünü ile tanıtıldı. Kalp atış hızı, koşu temposu, bisiklet temposu, kalori ve tur süresi gibi antrenman verileri, TCX dosyası içinde [XML](/tr/web/xml/) biçiminde saklanır. Ek olarak, antrenman parkuruyla ilgili özet veriler de TCX dosyasına dahildir. TCX dosyaları, Garmin giyilebilir spor cihazlarıyla oluşturulan [FIT](/tr/gis/fit/) dosyalarına benzer.

## TCX Dosya Biçimi - Daha fazla bilgi

TCX dosyaları, her kayıt bir etkinlik olarak kaydedilen XML dosyaları olarak diske kaydedilir. Bir aktivite, [GPX]'e benzer enlem-uzun konum için zaman damgasıyla birlikte konum çiftlerini içeren zaman, tur süresi, Kimlik, kalp atış hızı, yoğunluk, kadans ve parkur bilgileri gibi bir antrenmanın tüm verilerini içerir. (/tr/gis/gpx/) dosyaları.

### TCX Dosya Formatı Sürümleri

Garmin tarafından barındırılan kendi XML şemalarına sahip bu formatın iki versiyonu vardır. Aşağıdakiler bunlardan birkaçıdır:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX Veri Protokolü

TCX XML biçiminin hızlı bir sürümü Github'da [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol) olarak mevcuttur.

## Referanslar ##

* [Eğitim Merkezi XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Görüntüleyici](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

