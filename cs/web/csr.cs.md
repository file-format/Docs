{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor CSR - Formát souboru žádosti o podepsání certifikátu",
  "description" :"Zjistěte, co je soubor CSR a rozhraní API, která mohou vytvářet a otevírat soubory CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Co je soubor CSR?

Soubor CSR je soubor **Certificate Signing Request**, který se používá k vyžádání certifikátu SSL/TLS. Když potřebujete mít svůj SSL/TLS certifikát, vygenerujete CSR na stejném serveru, kde bude nakonec nainstalován. Tento soubor CSR je sdílen s certifikační autoritou (CA) za účelem vytvoření certifikátu. Obsahuje informace, jako je běžný název, organizace, země, a co je důležitější, **veřejný klíč**, který je integrován do vašeho souboru certifikátu a je podepsán odpovídajícím soukromým klíčem.

Aplikace, které mohou **otevřít soubory CSR**, zahrnují OpenSSL a Microsoft IIS.

## Formát souboru žádosti o podpis certifikátu

Soubor CSR je vytvořen ve formátu Base-64 PEM, který lze otevřít a zobrazit v jednoduchém textovém editoru, jako je Microsoft Notepad. Obsahuje záhlaví **-----ZAČÁTEK NOVÉ ŽÁDOSTI O CERTIFIKÁT-----** na začátku souboru a zápatí **-----KONEC NOVÉHO ŽÁDOSTI O CERTIFIKÁT-----** na konec souboru.

### Jak vypadá soubor CSR?

Jednoduchý příklad souboru CSR je následující.

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

## Jaké informace obsahuje CSR?

Soubor CSR obsahuje následující informace.

1. „Informace o firmě a webových stránkách“ – Zahrnuje informace, jako je běžné jméno, organizace, organizační jednotka, město/lokalita, stát/kraj/oblast (S), země a e-mailová adresa
1. `Veřejný klíč` - Je součástí certifikátu a používá se k šifrování přenášených dat, která jsou dešifrována pomocí odpovídajícího soukromého klíče
1. „Informace o typu a délce klíče“ – Obvykle se jedná o RSA 2048, ale může být také ve větších velikostech, jako je RSA 4096+

## Reference

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

