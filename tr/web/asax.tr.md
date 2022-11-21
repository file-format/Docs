{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax dosyası", "asax dosya biçimi", "asax dosya türü", "dosya", "tür", "asax dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET Sunucu Uygulama Dosyası",
  "description" :"ASAX dosyasının ne olduğunu ve ASAX dosyalarını oluşturabilen ve açabilen API'leri öğrenin.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## ASAX dosyası nedir?

.asax uzantılı bir dosya, sunucu tarafında bulunan ASP.NET uygulamaları tarafından kullanılan bir dosyadır. ASP.NET veya HTTP modülleri tarafından oluşturulan uygulama düzeyinde ve oturum düzeyinde olaylara yanıt vermek için kod içerir. Bu, uygulama başlatıldığında veya kapatıldığında belirli olayların işlenmesini de içerir. ASAX dosyaları isteğe bağlıdır ve uygulama düzeyindeki olayları ve hataları küresel düzeyde işlemek için web uygulamalarına yalnızca tek bir ASAX dosyası eklenir. ASPX sayfalarının aksine, ASAX dosyaları, uygulamanın işlevselliğini uygulamak için herhangi bir kod içermez.

## ASAX Dosya Biçimi

ASAX dosyaları düz metin dosyası biçiminde yazılır ve insanlar tarafından okunabilir. En sık kullanılan ASAX dosyası, bir ASP.NET uygulamasının kök dizininde bulunan Global.asax dosyasıdır. Web Sunucuları, kullanıcıların bu dosyanın kodunu indirmesini veya görüntülemesini yasaklamak için bu dosyaya gelen tüm çağrıları reddedecek şekilde yapılandırılmıştır.

### Global.ASAX - ASAX Dosya Biçimi Örneği

Tek bir ASAX dosyası, uygulama düzeyindeki olayları işlemek için yazılmış birden çok bölümden oluşur. Bunlar aşağıdaki gibidir.

* **Uygulama Yönergeleri** - Uygulama yönergeleri, Global.asax dosyasını işlerken ASP.NET ayrıştırıcısı tarafından kullanılacak uygulamaya özel isteğe bağlı ayarları tanımlamak için kullanılan etiketlerdir. Bu yönergeler Global.asax dosyasının başlangıcında bulunur ve aşağıdaki gibi tanımlanır.

```
<%@ yönerge öznitelik=değer [öznitelik=değer … ]%>
```
* **Kod Bildirim Blokları** - Kod bildirim blokları, \ içindeki ASP.NET uygulama dosyalarına katıştırılmış sunucu kodu bölümlerini tanımlamak için kullanılır.<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Kod Oluşturma Blokları** - Bunlar, sayfa oluşturulduğunda yürütülen satır içi kodu veya ifadeleri tanımlar. İki kod oluşturma bloğu stili, satır içi kodu ve satır içi ifadeleri içerir. İlki, kendi kendine yeten satırları veya kod bloklarını tanımlamak için kullanılırken, yanal, Write yöntemini çağırmak için bir kısayol olarak kullanılır.

## Referanslar

* [HTTP İşleyicileri ve HTTP Modüllerine Genel Bakış](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax Söz Dizimi](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

