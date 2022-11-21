{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx dosyası", "asmx dosya biçimi", "asmx dosya türü", "dosya", "tür", "asmx dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web Servis Dosyası",
  "description" :"ASMX dosyasının ne olduğu ve ASMX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## ASMX dosyası nedir?

.asmx uzantılı bir dosya, Simple Object Access Protocol (SOAP) kullanarak internet üzerinden iki nesne arasında iletişim sağlayan bir ASP.NET Web Service dosyasıdır. Gelen isteği işlemek ve yanıtı döndürmek için Windows tabanlı Web Sunucusunda bir hizmet olarak dağıtılır. ASP.NET web sayfalarının görsel gösterimi için kod içeren [ASPX](/tr/web/aspx/) dosyalarının aksine, ASMX dosyaları sunucuda arka planda çalışır ve veritabanına bağlanma, veri alma ve geri döndürme gibi farklı görevleri yerine getirir. talebin yapıldığı format. Bunlar özellikle XML web hizmetleri için kullanılır.

## ASMX Dosya Biçimi

ASMX dosyaları düz metin biçimindedir ve Microsoft Visual Studio veya metin editörleri gibi uygulamalarda açılabilir veya düzenlenebilir. Microsoft'un tescilli bir dosya biçimidir ve web hizmetlerinin oluşturulması için iyi tanımlanmış bir sözdizimine sahiptir. SOAP XML biçiminde bir ASMX dosyası tarafından verilen yanıt aşağıdaki öğelere sahiptir.

* 'Zarf' - XML belgesini bir SOAP mesajı olarak tanımlayan bir kök öğe.
* "Başlık" - Kimlik doğrulama verileri gibi uygulamaya özgü bilgileri içeren isteğe bağlı bir öğe. Başlık öğesi mevcutsa, Zarf öğesinin ilk alt öğesi olmalıdır.
* `Gövde` - Alıcıya yönelik SABUN mesajını içerir.
* `Fault` - Hata mesajlarını belirtmek için kullanılan isteğe bağlı bir öğe. Fault öğesi varsa, Body öğesinin bir alt öğesi olmalıdır.

ASMX dosyaları, [C#](/tr/programming/cs/), [Visual Basic](/tr/programming/vb/) veya JScript gibi .NET dillerinde yazılabilir.

## ASMX'in ASPX ve ASCX'ten farkı nedir?

ASMX dosyaları, ASPX ve ASCX dosyalarından farklıdır.

* ASPX, Active Server Pages dosyaları, web sunucuları üzerinde çalışan Microsoft ASP.NET çerçevesi kullanılarak oluşturulmuş programlama dosyalarıdır. Bunlar, kullanıcı böyle bir sayfaya erişmek istediğinde müşterinin web tarayıcısında işlenir.
* ASCX, Aktif Sunucu Kullanıcı Kontrolü, ASP.NET web sayfalarında veya tüm web sitesinde yeniden kullanılabilir kontrolleri tanımlamak için kullanılan kullanıcı kontrollerini tanımlar.

## Referanslar

* [ASMX Hizmetini Kullanma](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX Kullanıcı Kontrolü](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

