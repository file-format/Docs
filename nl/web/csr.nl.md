{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR-bestand - bestandsindeling voor ondertekeningsverzoek",
  "description" :"Meer informatie over wat een CSR-bestand is en API's die CSR-bestanden kunnen maken en openen.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Wat is een CSR-bestand?

Een CSR-bestand is een **Certificate Signing Request**-bestand dat wordt gebruikt om een SSL/TLS-certificaat aan te vragen. Wanneer u uw SSL/TLS-certificaat nodig heeft, genereert u de CSR op dezelfde server waar deze uiteindelijk wordt geïnstalleerd. Dit CSR-bestand wordt gedeeld met de certificeringsinstantie (CA) voor het maken van het certificaat. Het bevat informatie zoals de algemene naam, organisatie, land en, belangrijker nog, de **openbare sleutel** die is geïntegreerd in uw certificaatbestand en is ondertekend met de bijbehorende privésleutel.

Toepassingen die **CSR-bestanden** kunnen openen, zijn onder meer OpenSSL en Microsoft IIS.

## Certificaat Ondertekening Verzoek Bestandsformaat

Een CSR-bestand wordt gemaakt in een Base-64 PEM-indeling die kan worden geopend en bekeken in een eenvoudige teksteditor zoals Microsoft Notepad. Het bevat een header **-----BEGIN NEW CERTIFICATE REQUEST-----** aan het begin van het bestand en een footer **-----END NEW CERTIFICATE REQUEST-----** op het einde van het bestand.

### Hoe ziet een CSR-bestand eruit?

Een eenvoudig voorbeeld van een CSR-bestand is als volgt.

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

## Welke informatie staat er in een CSR?

Een CSR-bestand bevat de volgende informatie.

1. 'Informatie over bedrijf en website' - Bevat informatie zoals algemene naam, organisatie, organisatie-eenheid, stad/plaats, staat/provincie/regio (S), land en e-mailadres
1. 'Public Key' - Het is opgenomen in het certificaat en wordt gebruikt om verzonden gegevens te coderen die worden gedecodeerd met de bijbehorende privésleutel
1. 'Informatie over het sleuteltype en de lengte' - Dit is meestal RSA 2048, maar kan ook in grotere maten voorkomen, zoals RSA 4096+

## Referenties

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

