{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR Faylı - Sertifikat İmzalama Sorğu Fayl Formatı",
  "description" : "CSR faylı və CSR faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-az",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## CSR faylı nədir?

CSR faylı SSL/TLS sertifikatı tələb etmək üçün istifadə edilən **Sertifikat İmzalama Sorğusu** faylıdır. SSL/TLS sertifikatınıza sahib olmaq lazım olduqda, siz CSR-ni nəhayət quraşdırılacağı eyni serverdə yaradırsınız. Bu CSR faylı sertifikatın yaradılması üçün Sertifikat Təşkilatı (CA) ilə paylaşılır. O, ümumi ad, təşkilat, ölkə və daha da əhəmiyyətlisi, sertifikat faylınıza inteqrasiya olunmuş və müvafiq şəxsi açarla imzalanmış **ictimai açar** kimi məlumatları ehtiva edir.

**CSR fayllarını** aça bilən proqramlara OpenSSL və Microsoft IIS daxildir.

## Sertifikat İmzalama Sorğunun Fayl Formatı

CSR faylı Microsoft Notepad kimi sadə mətn redaktorunda açılıb baxıla bilən Base-64 PEM formatında yaradılmışdır. Buraya faylın əvvəlində başlıq **-----YENİ SERTİFİKAT SORĞUNA BAŞLAYIN-----** və altbilgi **----- YENİ SERTİFİKAT SORĞUNU SON-----** faylın sonu.

### CSR faylı necə görünür?

CSR faylının sadə nümunəsi aşağıdakı kimidir.

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

## KSM-ə hansı məlumatlar daxildir?

CSR faylı aşağıdakı məlumatları ehtiva edir.

1. `Biznes və Vebsayt haqqında məlumat` - Ümumi Ad, Təşkilat, Təşkilat Bölməsi, Şəhər/Yer, Ştat/Şəhər/Region (S), Ölkə və E-poçt Ünvanı kimi məlumatları ehtiva edir
1. `İctimai Açar` - O, sertifikata daxildir və müvafiq şəxsi açardan istifadə etməklə deşifrə edilən ötürülən məlumatları şifrələmək üçün istifadə olunur.
1. `Açar növü və uzunluğu haqqında məlumat` - Bu adətən RSA 2048-dir, lakin RSA 4096+ kimi daha böyük ölçülərdə də ola bilər.

## İstinadlar

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)


