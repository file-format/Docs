{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD Dosyası - ASP.NET Web İşleyicisi Dosya Formatı",
  "description" :"AXD dosyasının ne olduğunu ve AXD dosyalarını oluşturup açabilen API'leri öğrenin.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## .AXD dosyası nedir?

AXD dosyası, ASP.NET'te gömülü kaynak isteklerini işlemek ve almak için kullanılan bir web ayarları dosyasıdır. Resimler, JavaScript ([.JS](/tr/web/js/)) dosyaları ve [.CSS](/tr/web/css/) dosyaları gibi gömülü kaynakları almaya yönelik talimatlardan oluşur. AXD dosyaları, kaynakları istemci tarafı sayfalara enjekte etmek için kullanılır. Bu, istemci sayfalarının sunucudaki bu kaynaklara standart bir şekilde erişmesine olanak tanır.

## AXD Dosya Formatı

AXD dosyaları sunucu tarafında ikili dosyalar olarak saklanır. ASP.NET'teki bir web sunucusuna yönelik belirli isteklere yanıtlar üreten bileşenler olan Web İşleyicisi dosyasını ifade eder. AXD dosyaları, istemci tarafı sayfa isteklerine göre yanıt oluşturmadan önce özel işlemler gerçekleştirir. Bunlar genellikle **WebResource.axd** dosyaları olarak kaydedilir.

### WebResource.axd dosyası nedir?

Çoğu ASP.NET projesi, AXD dosyalarını, istemci tarafı sayfaların bir derlemeye katıştırılmış kaynakları indirmesine olanak tanıyan WebResource.axd dosyaları olarak kaydeder. WebResources.axd işleyicisi önbelleğe alınmadığı için hata ayıklama modunda çalıştırmanız durumunda uygulamanız yavaş performansla karşılaşabilir.

## Referanslar

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

