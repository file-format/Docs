{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR-fil - Filformat for anmodning om certifikatsignering",
  "description" : "Lær om, hvad en CSR-fil og API'er er, der kan oprette og åbne CSR-filer.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-da",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Hvad er en CSR fil?

En CSR-fil er en **Certificate Signing Request**-fil, der bruges til at anmode om SSL/TLS-certifikat. Når du skal have dit SSL/TLS-certifikat, genererer du CSR'en på den samme server, hvor den til sidst skal installeres. Denne CSR-fil deles med Certificate Authority (CA) til oprettelse af certifikatet. Den indeholder oplysninger såsom almindeligt navn, organisation, land og, endnu vigtigere, den **offentlige nøgle**, der er integreret i din certifikatfil og er signeret med den tilsvarende private nøgle.

Programmer, der kan **åbne CSR-filer**, inkluderer OpenSSL og Microsoft IIS.

## Filformat for anmodning om certifikatsignering

En CSR-fil oprettes i et Base-64 PEM-format, der kan åbnes og ses i en simpel teksteditor, såsom Microsoft Notesblok. Den indeholder en header **-----BEGIN NY CERTIFIKATANMODNING-----** i starten af filen og en sidefod **-----SLUT NY CERTIFIKATANMODNING-----** kl. slutningen af filen.

### Hvordan ser en CSR-fil ud?

Et simpelt eksempel på en CSR-fil er som følger.

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

## Hvilke oplysninger er inkluderet i en CSR?

En CSR-fil indeholder følgende oplysninger.

1. Oplysninger om virksomhed og websted - Indeholder oplysninger såsom almindeligt navn, organisation, organisatorisk enhed, by/lokalitet, stat/amt/region (S), land og e-mailadresse
1. Public Key - Den er inkluderet i certifikatet og bruges til at kryptere transmitterede data, som dekrypteres ved hjælp af den tilsvarende private nøgle
1. `Information om nøgletype og længde` - Dette er normalt RSA 2048, men kan også komme i større størrelser såsom RSA 4096+

## Referencer

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)


