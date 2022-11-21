{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt dosyası", "crt dosya formatı", "crt dosya türü", "dosya", "tür", "crt dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Güvenlik Sertifikası Dosya Formatı",
  "description":"CRT dosya formatı ve CRT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## CRT dosyası nedir?

.crt uzantılı bir dosya, güvenli web siteleri tarafından web sunucusundan bir tarayıcıya güvenli bağlantılar kurmak için kullanılan bir güvenlik sertifikası dosyasıdır. Güvenli web siteleri, veri aktarımlarını, girişleri, ödeme kartı işlemlerini güvenli hale getirmeyi ve siteye korumalı göz atma olanağı sağlar. Güvenli bir web sitesi açarsanız, adres çubuğunda bir "kilit" simgesi görürsünüz. Üzerine tıklarsanız, kurulu sertifikanın ayrıntılarını görüntüleyebilirsiniz. Verisign ve Thawte gibi uluslararası şirketler bu SSL sertifikalarının dağıtımını yapmaktadır.

## CRT Dosya Biçimi

CRT dosyaları ASCII formatındadır ve sertifika dosyasının içeriğini görüntülemek için herhangi bir metin düzenleyicide açılabilir. Sertifikanın yapısını tanımlayan X.509 sertifika standardına uygundur. SSL sertifikasında bulunması gereken veri alanlarını tanımlar. CRT, Base64 ASCII kodlu dosyalar olan sertifikaların PEM formatına aittir.

### PEM Dosya Yapısı

Bir PEM dosyası birden çok sertifikaya sahip olabilir. Böyle bir durumda PEM dosyasındaki her sertifika aşağıdaki yapıyı takip eder.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### CRT Dosya Biçimi Örneği

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referanslar ##

* [Genel Anahtarlar, Özel Anahtarlar ve Sertifikalar](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

