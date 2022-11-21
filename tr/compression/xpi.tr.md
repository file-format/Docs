{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Platformlar Arası Yükleyici Paket Dosyası",
  "description":"XPI dosya formatı ve XPI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## XPI dosyası nedir?

Bir XPI dosyası, dosyanın boyutunu azaltmak için sıkıştırılmış bir yükleme arşividir. Eklentilerin ve eklenti dosyalarının kurulumu için Mozilla uygulamaları tarafından kullanılır. Bir dizi veri dosyasıyla birlikte dosyanın kökünde bir yükleme komut dosyası veya bir bildirim içerir. Bir XPI dosyası, kullanıcının Firefox tarayıcısı, Thunderbird veya SeaMonkey'in bir parçası olmak için yükleyebileceği temalar, araç seti veya Firefox eklentileri içerebilir.

## XPI Dosya Biçimi - Daha Fazla Bilgi

XPI dosyaları, birden çok dosyayı tek bir sıkıştırılmış dosyada birleştiren [ZIP](/tr/compression/zip/) arşivleri olarak diske kaydedilir. Bir XPI dosyasının içindeki dosyalar, JS gibi yükleme komut dosyasını ve [CSS](/tr/web/css/), [HTML](/tr/web/html/) ve [JSON](/tr/web/json/) gibi web dosyalarını içerebilir. ). Bazen, eklenti tarafından simge olarak kullanılacak [PNG](/tr/image/png/) görüntü dosyaları da içerebilir.

### XPI dosyasının içeriği nasıl görüntülenir?

Bir XPI dosyası, pratik olarak içeriği aşağıdaki adımlar kullanılarak görüntülenebilen bir ZIP arşividir.

* Dosyanın uzantısını XPI'den ZIP'e değiştirin
* Dosyanın içeriğini WinZip (Windows, Mac), 7-Zip (Windows) veya Apple Archive Utility (Mac) gibi herhangi bir standart açma yardımcı programını kullanarak çıkarın.

### Firefox Android'de XPI Dosyasını Kurun

Çoğu kişi, XPI dosyalarının Android cihazlarda Firefox'a yüklenip yüklenemeyeceğini merak ediyor. Android'de, dosyayı bulup Firefox ile açarak bir XPI dosyasından eklenti yükleyebilirsiniz.

## Referanslar

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [XPI Dosya Uzantısını nasıl açabilirim?](https://support.mozilla.org/en-US/questions/1009049)

