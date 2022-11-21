{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CSR - Format File Permintaan Penandatanganan Sertifikat",
  "description" :"Pelajari tentang apa itu file CSR dan API yang dapat membuat dan membuka file CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Apa itu file CSR?

File CSR adalah file **Permintaan Penandatanganan Sertifikat** yang digunakan untuk meminta sertifikat SSL/TLS. Saat Anda perlu memiliki sertifikat SSL/TLS, Anda membuat CSR di server yang sama tempat akhirnya akan dipasang. File CSR ini dibagikan dengan Otoritas Sertifikat (CA) untuk pembuatan sertifikat. Ini berisi informasi seperti nama umum, organisasi, negara, dan, yang lebih penting, **kunci publik** yang terintegrasi dalam file sertifikat Anda dan ditandatangani dengan kunci pribadi yang sesuai.

Aplikasi yang dapat **membuka file CSR** termasuk OpenSSL dan Microsoft IIS.

## Format File Permintaan Penandatanganan Sertifikat

File CSR dibuat dalam format Base-64 PEM yang dapat dibuka dan dilihat dalam editor teks sederhana seperti Microsoft Notepad. Itu termasuk header **-----MULAI PERMINTAAN SERTIFIKAT BARU-----** di awal file dan footer **-----AKHIR PERMINTAAN SERTIFIKAT BARU-----** di akhir berkas.

### Bagaimana tampilan file CSR?

Contoh sederhana file CSR adalah sebagai berikut.

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

## Informasi apa saja yang termasuk dalam CSR?

File CSR berisi informasi berikut.

1. `Informasi tentang Bisnis dan Situs Web` - Termasuk informasi seperti Nama Umum, Organisasi, Unit Organisasi, Kota/Lokal, Negara Bagian/Kabupaten/Wilayah (S), Negara, dan Alamat Email
1. `Kunci Publik` - Ini termasuk dalam sertifikat dan digunakan untuk mengenkripsi data yang dikirimkan yang didekripsi menggunakan kunci pribadi yang sesuai
1. `Informasi tentang Jenis dan Panjang Kunci` - Ini biasanya RSA 2048 tetapi mungkin juga tersedia dalam ukuran yang lebih besar seperti RSA 4096+

## Referensi

* [Server Aplikasi Konsep](https://github.com/Devronium/ConceptApplicationServer)

