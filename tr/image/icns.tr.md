{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "uzantı", "dosya", "biçim", "görüntü", "Apple Simge Görüntüsü", "macOS", "Apple", "Simge"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Apple Simge Görüntüsü",
  "description":"ICNS dosya formatı ve ICNS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Bir ICNS dosyası nedir? ##

macOS programları tarafından kullanılan bir simge formatına ICNS dosyası denir. 1-bit ve 8-bit alfa bantlarına izin verir ve genellikle [PNG](/tr/image/png) belgelerinden yapılan bir veya daha fazla resmi kaydeder. macOS tarayıcısındaki ve arayüzündeki program simgesi, ICNS dosyaları kullanılarak görüntülenir.

Konuma bağlı olarak, aynı stil ikonunun birden çok ayarı olabilir. ICNS formatı çok sayıda değişikliğe uğradı ve artık çeşitli uyumlu formatların temeli olarak kullanılabileceği bir noktaya geldi. İşte bilmeniz gereken diğer bazı önemli noktalar:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource ve Mac OS simgeleri Resource diğer isimlerden bazılarıdır.
* Simge bilgisi için kaynak dalındaki bir kaynak kullanılır.
* Çoğu durumda, bir dosya çok sayıda resim içerir. 1612 piksel kare ve 1024, 512, 256, 128, 48, 32 ve 16 piksel kare desteklenen resim boyutlarıdır.


## ICNS Dosya Biçimi ##

ICNS veri formatı, 1 bitlik bantları ve çok sayıda görüntü durumunu destekleyen, bir veya daha fazla görüntü için bir kapsüldür.
İşletim sistemi, gerekli ekran boyutuna sığdırmak için simge resimlerini yeniden boyutlandırabilir. Daha büyük simge resimleri genellikle [JPEG](/tr/image/jpeg/) 2000 veya [PNG](/tr/image/png) dosyaları olarak kaydedilir. Hem sıkıştırılmış hem de sıkıştırılmamış ICNS dosyalarının bir türü mümkündür.

Bir başlık ve ikili simge verileri, bir ICNS dosyasının yapısını oluşturur. Başlık, dördü sihirli hazır bilgi ve dördü dosyanın uzunluğu olan 8 baytlık veri içerir. Her bir ikon resminin türü ve boyutu, ardından ikili resim verilerinin geldiği ikon verileri bölümünde saklanır. Resim boyutu, ikili bölümün boyutunu belirler.

## Teknik Şartname ##

### Başlık ###

|Ofset|Boyut|Amaç
---|---|---|
|0|4|Sihirli hazır bilgi, "icns" olmalıdır (0x69, 0x63, 0x6e, 0x73)
|4|4|Dosya uzunluğu, bayt cinsinden, önce msb


### Simge verileri ###

|Ofset|Boyut|Amaç
---|---|---|
|0|4|Simge türü
|4|4|Verinin uzunluğu, bayt cinsinden (tür ve uzunluk dahil), önce msb
|8|Değişken|Simge verileri

### Sıkıştırma ###

Piksel verileri bir dereceye kadar sıkıştırılmıştır. 32-bit ("is32", "il32", "ih32", "it32") ve ARGB ("ic04", "ic05") pikselleri genellikle PackBits'e benzer şekilde (kanal başına) sıkıştırılır.

|Kurşun Değeri|Kuyruk Baytları|Sonuç (sıkıştırılmamış)
---|---|---|
|0 - 127|1 - 128|1 - 128 Bayt
|128 - 255|1 Bayt|3 - 130 Kopya

## Referans ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

