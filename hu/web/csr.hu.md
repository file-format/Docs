{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR-fájl – Tanúsítvány-aláírási kérelem fájlformátuma",
  "description" :"További információ arról, hogy mi az a CSR-fájl és az API-k, amelyek CSR-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Mi az a CSR-fájl?

A CSR-fájl egy **Certificate Signing Request** fájl, amely SSL/TLS-tanúsítvány kérésére szolgál. Ha szüksége van az SSL/TLS-tanúsítványra, a CSR-t ugyanazon a kiszolgálón kell létrehoznia, ahol az végül telepítve lesz. Ez a CSR-fájl meg van osztva a tanúsító hatósággal (CA) a tanúsítvány létrehozásához. Olyan információkat tartalmaz, mint a közönséges név, szervezet, ország, és ami még fontosabb, a **nyilvános kulcs**, amely a tanúsítványfájlba integrálva van, és a megfelelő privát kulccsal van aláírva.

A **CSR-fájlok megnyitására** képes alkalmazások közé tartozik az OpenSSL és a Microsoft IIS.

## Tanúsítvány-aláírási kérelem fájlformátuma

A CSR-fájl Base-64 PEM formátumban jön létre, amely megnyitható és megtekinthető egy egyszerű szövegszerkesztőben, például a Microsoft Notepadben. Tartalmaz egy fejlécet **-----KEZDŐ ÚJ TANÚSÍTVÁNYKÉRÉS-----** a fájl elején és egy láblécet **-----END ÚJ TANÚSÍTVÁNYKÉRÉS-----** a fájl vége.

### Hogyan néz ki egy CSR-fájl?

A CSR-fájl egyszerű példája a következő.

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

## Milyen információkat tartalmaz a CSR?

A CSR-fájl a következő információkat tartalmazza.

1. „Információk az üzletről és a webhelyről” – olyan információkat tartalmaz, mint a közönséges név, szervezet, szervezeti egység, város/helység, állam/megye/régió (S), ország és e-mail cím
1. „Nyilvános kulcs” – A tanúsítvány tartalmazza, és a továbbított adatok titkosítására szolgál, amelyeket a megfelelő privát kulccsal dekódolnak.
1. "Információk a kulcs típusáról és hosszáról" - Ez általában RSA 2048, de előfordulhat nagyobb méretben is, például RSA 4096+

## Hivatkozások

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

