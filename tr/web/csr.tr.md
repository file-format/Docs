{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR Dosyası - Sertifika İmzalama Talebi Dosya Formatı",
  "description" :"CSR dosyasının ne olduğu ve CSR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## CSR dosyası nedir?

Bir CSR dosyası, SSL/TLS sertifikası istemek için kullanılan bir **Sertifika İmzalama İsteği** dosyasıdır. SSL/TLS sertifikanıza ihtiyacınız olduğunda, CSR'yi son olarak kurulacağı aynı sunucuda oluşturursunuz. Bu CSR dosyası, sertifikanın oluşturulması için Sertifika Yetkilisi (CA) ile paylaşılır. Ortak ad, kuruluş, ülke ve daha da önemlisi sertifika dosyanıza entegre edilmiş ve karşılık gelen özel anahtarla imzalanmış **ortak anahtar** gibi bilgileri içerir.

**CSR dosyalarını açabilen** uygulamalar arasında OpenSSL ve Microsoft IIS bulunur.

## Sertifika İmzalama İsteği Dosya Biçimi

Microsoft Notepad gibi basit bir metin düzenleyicide açılıp görüntülenebilen Base-64 PEM biçiminde bir CSR dosyası oluşturulur. Dosyanın başında **-----BEGIN NEW CERTIFICATE REQUEST-----** üst bilgisini ve dosyanın başında **-----END NEW CERTIFICATE REQUEST-----** altbilgisini içerir. dosyanın sonu.

### Bir CSR dosyası nasıl görünür?

Basit bir CSR dosyası örneği aşağıdaki gibidir.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## Bir CSR'de hangi bilgiler yer alır?

Bir CSR dosyası aşağıdaki bilgileri içerir.

1. "İşletme ve Web Sitesi Hakkında Bilgiler" - Ortak Ad, Kuruluş, Kuruluş Birimi, Şehir/Yer, Eyalet/İlçe/Bölge (S), Ülke ve E-posta Adresi gibi bilgileri içerir
1. "Genel Anahtar" - Sertifikaya dahildir ve ilgili özel anahtar kullanılarak şifresi çözülen iletilen verileri şifrelemek için kullanılır.
1. "Anahtar Türü ve Uzunluğu Hakkında Bilgi" - Bu genellikle RSA 2048'dir ancak RSA 4096+ gibi daha büyük boyutlarda da olabilir.

## Referanslar

* [Konsept Uygulama Sunucusu](https://github.com/Devronium/ConceptApplicationServer)

