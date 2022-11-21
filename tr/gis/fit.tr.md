{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT Dosya Biçimi- Garmin Etkinlik Dosyası",
  "description":"FIT dosya formatı ve FIT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## .fit dosyası nedir?

Bir FIT dosyası, Garmin spor giyilebilir cihazları tarafından oluşturulan bir GIS dosyasıdır. Kişinin bu cihazları giyerek hareket ettiği esnada yaptığı aktiviteleri kayıt altına almak için kullanılmaktadır. Etkinlik verileri, GPS cihazı tarafından kaydedildiği şekliyle konum ve zamanı içerir. FIT dosyaları, kaydedilen etkinlik verilerini web API'leri kullanarak aktarmak için de kullanılır. FIT dosyalarının, fitness verilerini diğer fitness platformlarıyla paylaşmak için en sık kullanılan dosya biçimi olmasının nedeni budur. Diğer yaygın dosya biçimleri arasında [GPX](/tr/gis/gpx/), TCX ve [KML](/tr/gis/kml/) bulunur.

## FIT Dosya Biçimi - Daha Fazla Bilgi

FIT dosyaları, etkinlik için Garmin cihazları tarafından kaydedilen bilgilerle ikili dosyalar olarak diske kaydedilir. Bir FIT dosyasında depolanan bilgiler şunları içerir:

* Tarih ve saat
* Spor türleri
* Tur ve bölünmüş veriler
* GPS izi
* Sensör verileri
* Etkin oturum için etkinlikler

Etkinlik verileri dosyaya gerçek zamanlı olarak kaydedilebilir veya etkinlik kaydı tamamlandıktan sonra dışa aktarılabilir.

### FIT Etkinlik Mesajları

Bir FIT etkinlik dosyası, bazı gerekli mesaj türlerini içerebilir. Bir aktivite dosyası için gerekli mesajlar aşağıdadır.

|Mesaj|Amaç|
---|---|
|Dosya Kimliği| Dosya Kimliği mesajı, tüm FIT dosya türleri için gereklidir ve dosyadaki ilk mesaj olması beklenir. Activity dosyaları için Type özelliği 4 olarak ayarlanmalıdır.|
|Aktivite| Bir FIT Etkinlik dosyasında tek bir Etkinlik mesajı gereklidir. Etkinlik mesajına, Yerel Zaman Damgası ve Oturum Sayısı özellikleri dahildir. Yerel Zaman Damgası, dosyadaki tüm zaman damgalarına uygulanabilen saat dilimi farkını belirlemek için kullanılır. Çoğu cihaz, FIT dosyalarını gerçek zamanlı olarak kaydeder ve oturum sayısı, kaydın sonuna kadar bilinemez. Bu nedenle Activity mesajı genellikle dosyadaki son mesaj olur.|
|Oturum| Etkinlik dosyaları bir veya daha fazla Oturum mesajı içerecektir. Oturum mesajı, Özet mesaj türüdür. Başlangıç Zamanı, Toplam Geçen Süre, Toplam Zamanlayıcı Süresi ve Zaman Damgası, tüm özet mesajları için doldurulması zorunlu alanlardır.|
|Kucak| Tur mesajları, seans içindeki turları veya aralıkları temsil eder. Tur mesajı, Özet mesaj türüdür. Başlangıç Zamanı, Toplam Geçen Süre, Toplam Zamanlayıcı Süresi ve Zaman Damgası, tüm özet mesajları için doldurulması zorunlu alanlardır.|
|Kayıt| Kayıt mesajları arasında GPS koordinatı, hız, mesafe, kalp atış hızı, güç vb. bulunur.|

## FIT Dosyası Yararlı Kaynaklar

* [FIT Etkinlik Dosyalarının Kodunu Çözme](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [FIT Etkinlik Dosyalarını Kodlama](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referanslar ##

* [FIT Etkinlik Dosyası](https://developer.garmin.com/fit/file-types/activity/)

