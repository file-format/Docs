{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx dosyası", "ascx dosya biçimi", "ascx dosya türü", "dosya", "tür", "ascx dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX Dosya Biçimi",
  "description" :"ASCX dosyasının ne olduğu ve ASCX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ASCX dosyası nedir?

.ascx uzantılı bir dosya, web sayfalarında yeniden kullanılabilir bir bileşen olarak kullanılan bir kullanıcı kontrolüdür. Herhangi bir ASP web sitesinde, kontrol kutusundan sayfaya sürüklenerek başvurulur. ASCX kullanıcı kontrolleri, projeye merkezi bir kaynak olarak eklenir ve kullanıcı kontrolündeki herhangi bir değişikliğin tüm web sitesine yansıması sağlanır. İnternet üzerinden 2 nesne içinde iletişim kurmak için bir mekanizma tanımlayan ASMX dosyalarının aksine, ASCX dosyaları sayfalara veya web sitesine gömmek için kullanıcı kontrolleridir.

## ASCX Dosya Biçimi

ASCX dosyaları düz metin biçiminde yazılır ve .ascx.cs ile biten web sayfaları gibi özelliklerin arkasındaki kodu kullanabilir. Kullanıcı kontrollerinin biçimlendirme kodu, aşağıdaki örnekte gösterildiği gibi @Control yönergesi ile başlar.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Bu web kullanıcı kontrolü, sayfa altbilgisi, başlık veya bir tür site gezintisi gibi birçok sayfada yeniden kullanılabilir. Web kullanıcı denetimleri, diğer tüm denetimler gibi, onları görsel davranışlarını ayarlamada yararlı kılan özelliklere, yöntemlere ve olaylara sahiptir.

### Web.config'de kullanıcı kontrollerini kaydetme örneği

Tek bir kullanıcı kontrolünü birden fazla sayfada kullanabilmek için web kontrolü web.config'e kaydedilebilir. Bu, her sayfaya ayrı ayrı kaydolmak yerine tüm web sitesi üzerindeki kontrolün kullanılmasına izin verir. Aşağıdaki örnek kod, bir web kontrolünün web.config'de tüm web sitesinde alt bilgi olarak görüntülenecek şekilde nasıl kaydedileceğini tanımlar.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Referanslar

* [ASCX ve ASMX](https://forums.asp.net/t/1838934.aspx?How+to+work+with+ascx+files+)
* [ASCX Kullanıcı Kontrolü](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

