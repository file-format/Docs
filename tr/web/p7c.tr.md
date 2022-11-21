{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 Sertifika Dosyası",
  "description":"P7C dosya formatı ve P7C dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## P7C dosyası nedir?

Diğer güvenlik sertifikası dosyaları gibi bir P7C dosyası, ağ üzerinden kimlik doğrulamak için kullanılan bir dijital sertifikadır. Sertifika kullanan uygulamalar, bu sertifika dosyalarında bulunan ortak anahtarı kullanarak kimliği doğrular. Açık anahtarlı kriptografi veya asimetrik kriptografi, biri genel anahtar, diğeri özel anahtar olarak bilinen anahtar çifti kullanır. Özel anahtar, etkili güvenlik için güvende tutulurken, genel anahtar başkalarıyla paylaşılabilir. Diğer yaygın sertifika dosyası biçimleri arasında [CRT](/tr/web/crt/), DER ve PEM bulunur.

## P7C Dosya Biçimi - Daha Fazla Bilgi

P7C dosyaları diske ikili dosyalar olarak kaydedilir ve matematiksel problemlere dayalı kriptografik algoritmalar kullanılarak oluşturulan genel anahtar bilgilerini içerir. Bunlar herhangi bir metin düzenleyicide açılabilir ancak içerikleri insan tarafından okunabilir biçimde değildir. P7C dosyalarını açabilen uygulamalardan bazıları arasında Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Sertifika Yöneticisi ve Microsoft Windows Kişileri bulunur.

### P7C Dosya Biçimi Örneği

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referanslar ##

* [Genel Anahtar Şifreleme](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C dosyası nasıl oluşturulur?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

