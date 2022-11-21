{
  "date" : "2019-10-11",
  "keywords" :[ "tgs dosyası", "tgs dosya biçimi", "tgs dosyası nedir", "dosya", "tgs örneği", "tgs dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram Animasyonlu Çıkartma Dosya Formatı",
  "description":"TGS dosya formatı ve TGS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .tgs dosyası nedir?

.tgs uzantılı bir dosya, platformlar arası mesajlaşma hizmeti [Telegram](https://core.telegram.org/animated_stickers) tarafından sunulan animasyonlu bir çıkartma dosyasıdır. Animasyonlu çıkartmalar, hareketsiz görüntüler olan statik grafiklerin aksine, mesajlaşma uygulamaları kullanıcıları tarafından mesajlarda daha gelişmiş ve canlı içerik göndermek için kullanılır. Telegram başlangıçta hareketsiz görüntü etiketleri için [WEBP](/tr/image/webp/) dosya biçimini kullandı. TGS dosya biçimi, statik WEBP etiketleri ile karşılaştırıldığında animasyon verilerini daha yüksek çözünürlüklerde ve daha küçük dosya boyutlarında depolayabilir. TGS dosyaları, Telegram, 7-zip, Apple Archive Utility ve Corel WinZip gibi uygulamalar kullanılarak açılabilir.

## TGS Dosya Biçimi

Telegram, TGS dosya formatını Temmuz 2019'da Lottie kütüphanesine dayalı olarak tanıttı. Bir TGS dosyası, Adobe After Effects'teki bir animasyondan dışa aktarılan [JSON](/tr/web/json/) metninden oluşur. Dışa aktarılan JSON metni, dosya boyutunu azaltan gzip sıkıştırması kullanılarak sıkıştırılır. Metin dosyasıyla ilgili JSON bilgisi, yüksek sıkıştırma oranlarının temeli haline gelen metin dosyasında saklanır.

### TGS Etiketleri Özellikleri

TGS dosya formatı, TGS animasyonlu çıkartmaların oluşturulmasına belirli sınırlamalar getirir. Bir TGS animasyon dosyası:

* Çıkartma/tuval boyutu 512х512 piksel olmalıdır.
* Çıkartma nesneleri tuvalin dışına çıkmamalıdır.
* Animasyon uzunluğu 3 saniyeyi geçmemelidir.
* Tüm animasyonlar döngülü olmalıdır.
* Bodymovin'de oluşturulduktan sonra etiket boyutu 64 KB'yi geçmemelidir.
* Tüm animasyonlar Saniyede 60 Kare hızında çalışmalıdır.

### Örnek TGS JSON Metni

Örnek bir animasyonlu çıkartma sıkıştırılmış haldeyken aşağıdaki JSON metin içeriğini içerir.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referanslar ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Vikipedi](https://en.wikipedia.org/wiki/Gzip)

