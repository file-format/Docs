{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Dosya", "Uzantı", "Dosya Formatı", "Dosya Uzantısı", "JSON", "Arşiv Dosyası"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP Arşiv Dosya Biçimi",
  "description" :"HAR dosyasının ne olduğunu ve HAR dosyasını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## HAR dosyası nedir?

.har ([HTTP](/tr/web/http/) Arşiv) dosyasına sahip bir dosya, birçok tarayıcı (Chrome, Safari, IE, Firefox vb.) üzerinden aktarılan oturum verilerini [JSON] içinde depolayan bir HTTP arşiv dosyasıdır. (/tr/web/json/) dosya biçimi. Sunucu ve istemci (bu durumda kullanıcının tarayıcısı) arasında internet üzerinden aktarılan veriler, HAR dosyasında saklanan HTTP istek ve yanıt başlıklarını içerir. Ayrıca, tarayıcıda yüklenen web sayfalarıyla ilgili performans verileri hakkında ayrıntılı bilgiler içerir. HAR dosyaları, Microsoft Windows işletim sistemindeki Not Defteri ve Apple MacOS'taki TextEdit gibi herhangi bir metin düzenleyicide açılabilir.

## HAR Dosya Biçimi - Daha Fazla Bilgi

HAR dosyaları, oturum bilgilerini popüler JSON formatını kullanarak düz metin dosyasında saklar. HAR dosya formatının belirtimleri, World Web Consortium'un (W3C) Web Performance Group tarafından üretilmiş ancak yayınlanamamıştır. Ancak, HTTP işlemleri için başarıyla bir arşiv formatı tanımladı.

İstek ve yanıt bilgilerinin aktarımını izlemeye ek olarak, HAR dosyaları, geliştiriciler tarafından web tarayıcısının performansını sayfa yükleme hızı, içerik yükleme süresi, yüklenen içerik, tarayıcıdan yanıt almak için yürütülen sorgular ve diğer pek çok açıdan günlüğe kaydetmek için kullanılır. .

## Neden HAR dosyalarını kullanmalı?

HAR dosyaları, uzun yükleme sürelerini, sayfa oluşturma sürelerini ve yanıt sürelerini değerlendirerek bir web sitesinin performansını iyileştirmede yardımcı olabilir. HAR dosyaları, bu tür sorunları bulmak ve performansı artırmak için web sitesiyle ilgili sorunları çözmek için analiz edilebilir.

## HAR dosyası nasıl oluşturulur?

Peki, bir HAR dosyası nasıl oluşturulur? Bu, bir HAR dosyası oluşturmak için ne tür bir tarayıcı kullandığınıza bağlıdır. Bu kılavuzda, Google Chrome tarayıcısı için adımları listeliyoruz. Safari, Firefox vb. kullanarak HAR dosyaları oluşturma yöntemleri internette kolayca aranabilir ve takip edilebilir.

### Google Chrome kullanarak HAR dosyası oluşturma adımları

Aşağıdaki adımlar, sorunların yaşandığı bir web sayfasında gerçekleştirilebilir.

1. Google chrome'da sorunun oluştuğu web sayfasını açın.
1. Geliştirici aracını açın (öğeyi inceleyin).
1. Dosya kaydını başlatmak için panelin soluna gidin. Bu bölümde küçük yuvarlak kırmızı bir buton bulunmaktadır.
1. Tarayıcıda tutulan tüm günlük kayıtlarını silmek için “Simgeyi Temizle”ye tıklayın.
1. İstediğiniz içeriği yukarıda gösterildiği gibi kaydetmek için sağ tıklayın ve “HAR Dosyası Olarak Kaydet” seçeneğini tıklayın.

## Referanslar

* [HAR Dosya Biçimi - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

