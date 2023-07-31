{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ Derlenmiş Kaynak Komut Dosyası",
  "description":"RES örneği ve RES dosyalarını oluşturabilen ve açabilen API'ler ile RES dosya formatı hakkında bilgi edinin.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## RES dosyası nedir?
.res son ekine veya uzantısına sahip dosya, birçok dosya formatı kategorisine ait olabilir. Burada bir C++ Derlenmiş Kaynak Komut Dosyası olan RES dosya biçimini tartışıyoruz; kaynak verilerini içeren Microsoft Kaynak Derleyicisi (rc) tarafından oluşturulan bir ikili dosya; kaynak tanım dosyasının içeriğine göre; ana yazılım projesiyle ilgili. .res dosyası, onu bir uygulamanın yürütülebilir dosyasına bağlamak için genellikle bir kaynak nesne dosyası olarak yeniden biçimlendirilir.

## RES dosya formatı
RES dosya biçimi, Microsoft Kaynak Derleyicisine (rc) aittir. Kaynak derleyici, uygulamanızın kullandığı imleçler, simgeler, menüler ve iletişim kutuları gibi kaynakları derleyen bir araçtır. Kaynak dosyaları genellikle bir .res uzantısına sahiptir; imleçler, resimler ve sürüm bilgileri gibi kaynakları içerir. RES dosyası, 16 veya 32 bitlik bir kaynak dosyası olabilir.
## Kaynak dosya yapısı
Bir kaynak dosyası, bir dizi çeşitli kaynak girişi içerir. Her giriş bir kaynak başlığı ve ilgili verileri içerir. Bir kaynak başlığı genellikle dosyada DWORD ile hizalanır ve aşağıdakileri içerir:

- Kaynak başlığının boyutunu belirtmek için bir **DWORD**
- Kaynak verilerinin boyutunu belirtmek için bir **DWORD**
- kaynak türü
- kaynak adı
- Ek kaynak bilgileri

Kaynak başlık yapısı, RES dosyasının biçimini tanımlar. Kaynağın verileri, kaynak başlığını takip eder. Bazı kaynaklar, bir grup kaynak hakkında bilgi sağlamak için kaynağa özgü bir grup üst bilgi kalıbı da ekler. Aşağıda, kaynak giriş türlerinden bazıları ve açıklamaları yer almaktadır:

### Hızlandırıcı Tablo Kaynakları
Hızlandırıcı tablosu, grup başlığı olmayan bir RES dosyasındaki bir kaynak girişidir. **ACCELTABLEENTRY** kalıbı, hızlandırıcı tablosundaki her girişi tanımlar. Bir RES dosyası, Birden çok hızlandırıcı tablosuna sahip olabilir.

### İmleç ve Simge Kaynakları
Sistem her simgeyi ve imleci tek bir dosya olarak kabul etse de, bunlar RES dosyalarında bir grup simge kaynağı veya bir grup imleç kaynağı olarak depolanır. Simge ve imleç kaynaklarının dosya biçimleri aynıdır. Bir kaynak grubu üstbilgisi, .res dosyasındaki tüm bağımsız simge veya imleç grubu bileşenlerini takip eder.

### İletişim Kutusu Kaynakları
RES dosyasında bir kaynak girişi olarak bir iletişim kutusu da gerçekleştirilir. Bir **DLGTEMPLATE** iletişim kutusu başlık kalıbı ve iletişim kutusundaki her belirli kontrol için bir **DLGITEMPLATE** kalıbı içerir. **DLGTEMPLATEEX** ve **DLGITEMTEMPLATEEX** kalıpları, genişletilmiş iletişim kutusu kaynaklarının biçimini açıklar.

### Yazı Tipi Kaynakları
Bir menü kaynağı, menü şablonundaki her menü öğesi için bir tane olmak üzere bir veya daha fazla **NORMALMENUITEM** veya **POPUPMENUITEM** modelini izleyen bir **MENUHEADER** modeli içerir. **MENUEX_TEMPLATE_HEADER** ve **MENUEX_TEMPLATE_ITEM** kalıpları, genişletilmiş menü kaynaklarının biçimini açıklar.

### Mesaj Tablosu Kaynakları
Bir mesaj tablosu, bir hata mesajı olarak veya bir mesaj kutusunda görüntülenmek üzere biçimlendirilmiş metinden oluşur. Bir mesaj tablosu kaynağındaki ana kalıp, **MESSAGE_RESOURCE_DATA** yapısıdır.

### Sürüm Kaynakları
Sürüm kaynağındaki ana model **VS_FIXEDFILEINFO**'dur. Ek modeller, dil bilgileriyle ilgili verileri depolamak için **VarFileInfo** ve özel dize bilgileri için **StringFileInfo** içerir.




## Referanslar

* [Kaynak Dosya Biçimleri](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



