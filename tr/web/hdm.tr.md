{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM Dosyası - Elde Taşınabilir Cihaz İşaretleme Dili Dosyası",
  "description":"HDM dosya formatı ve HDM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Bir HDM dosyası nedir?

Bir HDM dosyası, Elde Taşınabilir Cihaz İşaretleme Dili'nde (HDML) oluşturulan bir biçimlendirme dili web sayfası dosyasıdır. [HTML](/tr/web/html/) diline benzer biçimlendirme etiketleri içerir, ancak akıllı telefonlar ve PDA'lar gibi elde taşınan elektronik cihazlar için tasarlanmıştır. [HDML dosya formatı özellikleri](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) standardizasyon için W3C'ye gönderildi ancak bir standart haline gelemedi. HDM, W3 web sitesinde bulunan [HDML](/tr/web/hdml/) dosya formatı özelliklerine dayalıdır.

## HDM Dosya Biçimi - Daha Fazla Bilgi

HDM dosyası, elde taşınan cihazlarda görsel olarak tasarlanmış web sitesine işlenen biçimlendirme etiketlerinden oluşur. HDM dosyaları, HTML sayfaları için kullanılan HTTP protokolü yerine HDTP (Handheld Device Transport Protocol) protokolü kullanılarak cihazlara kopyalanır.

## HDML Dosya Öğeleri

Aşağıda, HDML için çalışma zamanı ortamı sağlayan ve kullanıcı aracısı olarak anılan öğelerin bir listesi bulunmaktadır.

|Öğe|Açıklama|
---|---|
|Kartlar|Bu, HDML'nin temel yapı taşıdır ve bilgi kartlarını görüntüler ve kullanıcının bunlarla etkileşime girmesine izin verir. |
|Desteler|HDML kartları birlikte desteler halinde gruplanır. Bir HDML destesi, URL [RFC1738] tarafından tanımlanması ve bir sunucudan talep edilen ve kullanıcı aracısı tarafından önbelleğe alınan içerik birimi olması bakımından HTML sayfasına benzer.|
|Eylemler|Eylemler PREV, SOFT1-SOFT8 ve HELP türünde olabilir. Bunlar soyuttur ve kullanıcı arayüzünde kullanıcı aracısına özel bir şekilde desteklenir.|
|Aktiviteler|Bir aktivite, tek bir mantıksal işlevi yerine getiren ilgili kartlar grubu gibidir. Bunlar bir veya daha fazla desteyi kapsayabilir. HDML gezinme ve durum modeli, etkinlikler etrafında yapılandırılmıştır.|
|Geçmişe dayalı gezinme|Kullanıcı aracısı, kullanıcıya gösterilen kartların geçmişini tutar. Erişilen her kart, kart geçmişine eklenir. Kullanıcı aracısı, kullanıcının geçmişteki bir önceki karta kolaylıkla geri gitmesini sağlar.|

## Referanslar

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML Spesifikasyonları - W3 Okulları](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

