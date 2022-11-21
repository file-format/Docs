{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "uzantı", "dosya", "biçim", "web", "sertifika", "dil"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Sertifika Dosya Formatı",
  "description":"CER dosya formatı ve CER dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## CER dosyası nedir? ##

.cer uzantılı bir dosya, sahip sertifikası ve belirli genel anahtar hakkında bazı bilgileri depolamaktan sorumludur. Bu dosya biçimi, özel anahtarları depolayamaz ve yalnızca bir sertifika olan x509'u depolama kapasitesine sahiptir. Özel olarak güvenli sertifika yetkilileri, tarama için güvenilir ve güvenli bir protokol olan HTTPS'ye ait olanlardır.
CER, sunucunuzun bir sertifikasıdır. Genellikle etki alanı için sertifika yetkilisi tarafından alınır. CER çoğunlukla [CRT](/tr/web/crt/) ile aynı kabul edilir, ancak her ikisi de SSL sertifikasının aynı biçimidir ancak farklı dosya adı uzantılarıdır.
Bunlar, yalnızca bir tarayıcı açarak ve kullanılan tarayıcının veya web sitesinin güvenliğini kontrol ederek işletim sistemlerinde kullanılabilir.

## Kısa Tarih ##

1995'te Thawte, ABD dışındaki herkese açık SSL (güvenli soket bağlantısı) sertifikaları sorununu çözen ilk sertifika yetkilisi oldu. Bundan sonra, 1995'ten 2020'ye kadar kurulan bir dizi yetkili var.

## CER Dosya Biçimi ##

Bu dosyalar basitçe
* PKC S#7, Base64 ASCII kodlamasını içerir
* Dosya uzantıları p7b veya p7cZ'dir.
* İkili içerik için sertifika DER veya pkcs12/pfx olacaktır.
Bazı benzersiz özelliklere sahip birçok sertifika dosyası türü vardır:
* .pem, usThawteificate bir kuruluşun bu formatı zincirleme yaptığında sertifikalar oluşturduğu iyi bilinmektedir.
* .arm, kendinden imzalı bir sertifika ayıklama yöntemi gerektiğinde, bu amaç için belirtilen biçim .arm'dır. Base-64 ASCII kodlamasında temsil edilir.
* .der, Binary verilerden oluşur. Bu, yalnızca tek bir sertifika için kullanılabileceği anlamına gelir.
* .pfx (PKC512), CA tarafından verilen bir sertifikaya veya kendinden imzalı bir sertifikaya karşılık gelen özel bir anahtardan oluşur. Bu biçim, bir SSL uygulamasının diğerine dönüştürülmesiyle iyi bilinir.


