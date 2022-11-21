{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"El Aygıtı İşaretleme Dili Dosyası",
  "description":"HDML dosya formatı ve HDML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## HDML dosyası nedir?

.hdml (Handheld Device Markup Language) uzantılı bir dosya, el bilgisayarları, akıllı telefonlar ve bilgi görüntüleme cihazları gibi taşınabilir elektronik cihazlar için web sayfaları oluşturmaya yönelik bir biçimlendirme dilidir. HDML'nin [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) dilinin bir uzantısı olduğu söyleniyor. HDML, HTML'ye benzer, ancak PDA, cep telefonları vb. gibi küçük ekranlara sahip kablosuz ve elde taşınan cihazlar içindir. Önemli bir etkiye sahip olduğu WML ile değiştirildi.

## HDML Dosya Biçimi - Daha Fazla Bilgi

HDML, HTML'ye benzer işaretleme etiketlerine dayalı, avuçiçi cihazlar için bir biçimlendirme dilidir. HDML, standardizasyon için W3C'ye sunuldu, ancak hiçbir zaman bir standart haline gelmedi. Bununla birlikte, dosya biçimi spesifikasyonları referans için [W3 web sitesinde](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) mevcuttur. [HDML dili için sözdizimi](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) geliştiricinin referansı için mevcuttur ve örnek uygulama geliştirme için kullanılabilir.

## HDML Öğeleri

Aşağıda, HDML için çalışma zamanı ortamı sağlayan ve kullanıcı aracısı olarak anılan öğelerin bir listesi bulunmaktadır.

|Öğe|Açıklama|
---|---|
|Kartlar|Bu, HDML'nin temel yapı taşıdır ve bilgi kartlarını görüntüler ve kullanıcının bunlarla etkileşime girmesine izin verir. |
|Desteler|HDML kartları birlikte desteler halinde gruplanır. Bir HDML destesi, URL [RFC1738] tarafından tanımlanması ve bir sunucudan talep edilen ve kullanıcı aracısı tarafından önbelleğe alınan içerik birimi olması bakımından HTML sayfasına benzer.|
|Eylemler|Eylemler PREV, SOFT1-SOFT8 ve HELP türünde olabilir. Bunlar soyuttur ve kullanıcı arabiriminde kullanıcı aracısına özel bir şekilde desteklenir.|
|Aktiviteler|Bir aktivite, tek bir mantıksal işlevi yerine getiren ilgili kartlar grubu gibidir. Bunlar bir veya daha fazla desteyi kapsayabilir. HDML gezinme ve durum modeli, etkinlikler etrafında yapılandırılmıştır.|
|Geçmişe dayalı gezinme|Kullanıcı aracısı, kullanıcıya gösterilen kartların geçmişini tutar. Erişilen her kart, kart geçmişine eklenir. Kullanıcı aracısı, kullanıcının geçmişteki bir önceki karta kolaylıkla geri gitmesini sağlar.|

## Referanslar

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML Spesifikasyonları - W3 Okulları](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

