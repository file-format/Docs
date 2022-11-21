{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM Dosyası - Gizliliği Artırılmış Posta Sertifikası Dosya Biçimi",
  "description":"PEM dosya formatı ve PEM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## .pem dosyası nedir?

PEM dosyası, bir web sunucusu ile tarayıcı arasında güvenli bir iletişim kanalı oluşturmak için kullanılan bir güvenlik sertifikası dosyasıdır. Base64 kodludur ve bir özel anahtar, sunucu sertifikası ve/veya diğer sertifikaların bir kombinasyonunu içerebilir. PEM dosyaları, kullanım açısından .der sertifika dosyalarına benzer, ancak ikili veriler yerine Base64 kodlu metin olarak depolanır. Diğer benzer sertifika dosyası formatları arasında [.cer](/tr/web/cer/) ve [.crt](/tr/web/crt/) dosyaları bulunur.

**PEM dosyalarını açabilen** uygulamalar, Microsoft Notepad ve Apple TextEdit gibi metin düzenleyicileri içerir.

## PEM Dosya Biçimi

PEM, verileri depolamak için kullanılan dosyanın yapısını ve kodlama türünü tanımlayan bir kapsayıcı dosya biçimidir. PEM dosyaları, insanlar tarafından okunamayan Base64 kodlu dosya biçimi olarak diskte depolanır. Standart, bir PEM dosyasının şununla başladığını tanımlar:

```
-----BEGIN <type>-----
```
ve şununla biter:
```
-----END <type>-----
```

Bunların içindeki diğer tüm içerikler base64 kodludur (büyük ve küçük harfler, rakamlar, + ve /). Tek bir PEM dosyası, diğer programlar tarafından kullanılabilen birden çok bloktan oluşabilir. Bir PEM dosyası birden çok sertifika içeriyorsa, her sertifika aşağıdaki gibi ayrı bloklarla ayrılır:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### PEM Dosyası Örneği

CERTIFICATE bloğuna sahip bir PEM dosyası genellikle aşağıdaki gibi görünür:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

RSA içeren bir PEM dosyası aşağıdaki gibi başlar.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referanslar ##

* [Genel Anahtar Şifreleme](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C dosyası nasıl oluşturulur?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

