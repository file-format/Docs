{
  "date" : "2021-08-27",
  "keywords" :[ "wsh dosyası", "wsh dosya biçimi", "wsh dosyası nedir", "dosya", "wsh örneği", "wsh dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSH dosya formatı ve WSH dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"WSH - Windows Komut Dosyası",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## .wsh dosyası nedir?
.wsh uzantılı bir dosya, VB veya VBS gibi belirli bir programlama dili komut dosyası için özellikler ve parametreler içerir. WSH'nin asıl ihtiyacı, bunları belirli komut dosyalarının yürütülmesini özelleştirmek için kullanmaktır. Çalıştırmak için WScript veya CScript gereklidir ve bunların her ikisi de Windows işletim sistemine dahildir. WSH dosyaları ilk olarak Windows 95'te yükleme disklerinde Denetim Masası için isteğe bağlı yapılandırılabilir ve yüklenebilir olarak ve ardından Windows 98'in varsayılan bir bileşeni olarak sağlandı.

## WSH dosya formatı
WSH (Windows Komut Dosyası Sistemi), yönetim, oturum açma komut dosyaları ve genel otomasyon dahil olmak üzere çeşitli amaçlar için kullanılabilir. WSH, betiklerin çalışması için bir ortam oluşturur. uygun betik motorunu çalıştırır ve betiğin birlikte çalışması için bir dizi hizmet ve nesne tahsis eder. Bu komut dosyaları, bir COM nesnesinden veya komut satırı modundan GUI modunda çalıştırılabilir ve kullanıcıya hem etkileşimli hem de etkileşimli olmayan komut dosyaları için esneklik sağlar.

### Örnekler
İşte 'OK' düğmesiyle bir mesaj görüntülemek için kök WSH COM nesnesi "WScript" kullanan bazı VBScript'leri gösteren çok basit bir örnek. Bu komut dosyası çalıştırıldığında, CScript veya WScript motoru çağrılacak ve çalışma zamanı ortamı kurulacaktır.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referanslar

* [Windows Komut Dosyası Sistemi - Wikipedia'dan](https://en.wikipedia.org/wiki/Windows_Script_Host)



