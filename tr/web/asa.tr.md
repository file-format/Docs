{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "dosya formatı", "dosya türü", ".asa dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP Yapılandırma Dosyası",
  "description" :"ASA dosyası nedir ve ASA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## ASA dosyası nedir?

ASA dosyası, [ASP](/tr/web/asp/)/ASP.NET projeleri için oluşturulan yapılandırma dosyasıdır. Uygulamada Küresel düzeyde erişilebilir olması amaçlanan değişkenlerin, içeriklerin ve işlevlerin bildirimlerini içerir. Projedeki tüm sayfalar bu değişkenlere ve işlevlere erişebilir, böylece bunları yeniden yazma gereksinimi ortadan kalkar. Böyle bir örnek, diğer ASP web sitesi sayfaları tarafından erişilebilmesi için kök dizinde saklanan Global.asa sayfasıdır. Global.asa dosyaları isteğe bağlıdır, ancak kullanılırsa her uygulamanın yalnızca bir Global.asa dosyası olabilir.

## ASA Dosya Biçimi - Daha Fazla Bilgi

ASA dosyaları, aşağıdaki bilgileri içeren düz metin dosyalarıdır.

* Uygulama olayları
* Oturum etkinlikleri
* \<object> bildirimler
* TypeLibrary bildirimleri
* #include direktifi

## ASA Dosyası Örneği

Bir Global.asa dosyası buna benzer bir şeye benzeyebilir.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referanslar

* [ASP Global.asa dosyası - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

