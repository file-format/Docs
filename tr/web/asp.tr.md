{
  "date" : "2019-10-11",
  "keywords" :[ "asp","asp dosyası", "asp dosya biçimi", "asp dosya türü", "dosya", "tür", "asp dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Aktif Sunucu Sayfaları Dosya Formatı",
  "description" :"ASP dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ASP dosyası nedir?

ASP, web sayfaları oluşturmak için bir geliştirme çerçevesi olan Aktif Sunucu Sayfaları anlamına gelir. Web isteklerine hizmet etmek için bilgisayar kodunun dahili bir sunucu tarafından yürütülmesini sağlar. Web tarayıcısı tarafından bir ASP dosyası için bir istek oluşturulduğunda, sunucu dosyayı okur ve dosyanın içindeki herhangi bir kodu/komut dosyasını çalıştırarak **[HTML](/tr/web/html/)** sonucunu oluşturur ve bu da sunucuya döndürülür. görüntülemek için tarayıcı.

Sunucu tarafından sunulan statik sayfalar olan HTML sayfalarının aksine, ASP dosyaları çalışma zamanında bir veritabanından veri isteklerini içerebilen dinamik içerikler oluşturur. ASP sayfaları genellikle .html yerine .asp uzantısını kullanır. Bir ASP dosyasının içindeki kod/komut dosyası sunucu tarafında yürütüldüğünden, istekte bulunan tarayıcı, sunulan sayfayı oluşturmak için kullanılan kodu göremez. Tüm modern tarayıcılar, sonuç olarak oluşturulan sayfaları görüntüleme yeteneğine sahiptir. Microsoft teknolojisi üzerine kurulu olan ASP ile oluşturulan sayfalar, Microsoft İnternet Bilgi Servisleri (IIS) sunucularında barındırılmaktadır.

## ASP Dosya Formatının Kısa Tarihi
ASP, yerini sunucu yan sayfalarını geliştirmenin ve yönetmenin daha modern ve daha verimli bir yolu olan ASP.NET'e bırakana kadar yalnızca birkaç revizyondan geçti. ASP desteği, Internet Information Services (IIS) ile birlikte varsayılan olarak dahildir. ASP, her birinde iyileştirmelerle üç farklı sürümde yayınlandı.

* ASP 1.0, Aralık 1996'da IIS 3.0'ın bir parçası olarak yayınlandı
* ASP 2.0, Eylül 1997'de IIS 4.0'ın bir parçası olarak yayınlandı
* ASP 3.0, Kasım 2000'de IIS 5.0'ın bir parçası olarak yayınlandı

## ASP İşlevsel Nesneleri

ASP dosyaları, kullanıcı isteklerini işlemek ve kullanıcılara sunulacak çıktı sayfaları oluşturmak için sunucu tarafı nesnelerini kullanır. Her nesnenin, istekleri ve yanıtları işlemek için bir dizi koleksiyonu, özelliği ve yöntemi vardır. Bu nesneler şunları içerir:

### İstek Nesnesi

Bir tarayıcı bir sunucudan bir sayfa istediğinde buna istek denir. Request nesnesi bir ziyaretçiden bilgi almak için kullanılır.

### Yanıt Nesnesi

ASP Response nesnesi, sunucudan kullanıcıya çıktı göndermek için kullanılır.

### Sunucu Nesnesi

ASP Sunucusu nesnesi, sunucudaki özelliklere ve yöntemlere erişmek için kullanılır. Veritabanlarına (ADO), dosya sistemine bağlantılara ve sunucuda kurulu bileşenlerin kullanımına izin verir.

### Oturum Nesnesi

Bir oturum nesnesi, sunucudan bir sayfa isteyen kullanıcının tarayıcısı ile sunucunun kendisi arasındaki bir bağlantı gibidir. Bu, ASP tarafından oluşturulan ve kullanıcının bilgisayarına gönderilen bir tanımlama bilgisi ile sağlanır. Session nesnesi, bir kullanıcı oturumu hakkında bilgi veya değişiklik ayarları depolar. Bilgiler bir Oturum nesnesinde saklanır ve bir uygulamanın tüm sayfaları arasında paylaşılır. Oturum değişkenlerinde saklanan ortak bilgiler ad, kimlik ve tercihlerdir. Sunucu, her yeni kullanıcı için yeni bir Oturum nesnesi oluşturur ve oturum sona erdiğinde Oturum nesnesini yok eder.

### Uygulama Nesnesi

Uygulama nesnesi, uygulamadaki birçok sayfa tarafından kullanılacak bilgileri (veritabanı bağlantı bilgileri gibi) tutar. Bilgilere herhangi bir sayfadan erişilebilir. Bilgiler tek bir yerden de değiştirilebilir ve değişiklikler otomatik olarak tüm sayfalara yansıtılır. Application nesnesi tıpkı Session nesnesi gibi herhangi bir sayfadaki değişkenleri depolamak ve bunlara erişmek için kullanılır.

### ASPERror Nesnesi

ASPError nesnesi, ASP 3.0'da uygulanmıştır ve IIS5 ve sonrasında mevcuttur. ASPError nesnesi, bir ASP sayfasındaki komut dizilerinde meydana gelen herhangi bir hatanın ayrıntılı bilgilerini görüntülemek için kullanılır.

**Not:** ASPError nesnesi, Server.GetLastError çağrıldığında oluşturulur, bu nedenle hata bilgilerine yalnızca Server.GetLastError yöntemi kullanılarak erişilebilir.

## Referanslar

* [ASP - W3C Tarafından](https://www.w3schools.com/asp/default.asp)
* [Basit ASP Sayfaları Oluşturma](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

