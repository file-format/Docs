{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 Sertifika Dosyası",
  "description":"P7C dosya formatı ve P7C dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## P7B dosyası nedir?

P7B dosyası, bir kişinin veya cihazın kimliğini doğrulamak için güvenli dijital sertifika içeren bir güvenlik sertifikası dosyasıdır. Bir [.cer](/tr/web/cer/) sertifika dosyasına benzer şekilde, dosya üzerinde sağ tıklama seçeneği kullanılarak "Sertifika Yükle" seçeneği kullanılarak bir P7B dosyası kurulabilir. P7B, CER dosya biçiminden farklı biçimlendirme seçeneği kullanır. Base64 (ASCII) kodlamasını kullanan bir veya daha fazla X.509 dijital sertifika dosyası içerir. P7B dosyaları bir [ZIP](/tr/compression/zip/) dosyası olarak alınır veya Sertifika Yetkilisinden alınır.

## P7B Dosya Biçimi

P7B dosyaları, herhangi bir metin düzenleyicide açılabilen düz ASCII dosyaları olarak saklanır. Okunabilirlik açısından anlamsız olan kodlanmış bir dize olan ortak anahtarı içerir.

### P7B Dosya Biçimi Örneği

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referanslar ##

* [Genel Anahtar Şifreleme](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C dosyası nasıl oluşturulur?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

