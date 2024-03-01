{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR-tiedosto – sertifikaatin allekirjoituspyynnön tiedostomuoto",
  "description" : "Lue lisää siitä, mikä on CSR-tiedosto ja API:t, jotka voivat luoda ja avata CSR-tiedostoja.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-fi",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Mikä on CSR-tiedosto?

CSR-tiedosto on **Certificate Signing Request** -tiedosto, jota käytetään SSL/TLS-varmenteen pyytämiseen. Kun tarvitset SSL/TLS-varmenteen, luot CSR:n samalle palvelimelle, johon se lopulta asennetaan. Tämä CSR-tiedosto jaetaan varmenteen myöntäjän (CA) kanssa varmenteen luomista varten. Se sisältää tietoja, kuten yleinen nimi, organisaatio, maa ja mikä tärkeintä, **julkinen avain**, joka on integroitu varmennetiedostoosi ja on allekirjoitettu vastaavalla yksityisellä avaimella.

Sovelluksia, jotka voivat **avata CSR-tiedostoja**, ovat OpenSSL ja Microsoft IIS.

## Varmenteen allekirjoituspyynnön tiedostomuoto

CSR-tiedosto luodaan Base-64 PEM -muodossa, joka voidaan avata ja tarkastella yksinkertaisessa tekstieditorissa, kuten Microsoft Notepadissa. Se sisältää otsikon **-----ALUE UUSI SERTIFIKAATIPYYNTÖ-----** tiedoston alussa ja alatunnisteen **-----END NEW SERTIFICATE REQUEST-----** osoitteessa tiedoston loppuun.

### Miltä CSR-tiedosto näyttää?

Yksinkertainen esimerkki CSR-tiedostosta on seuraava.

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

## Mitä tietoja CSR sisältää?

CSR-tiedosto sisältää seuraavat tiedot.

1. Tiedot yrityksestä ja verkkosivustosta - Sisältää tietoja, kuten yleinen nimi, organisaatio, organisaatioyksikkö, kaupunki/paikkakunta, osavaltio/maakunta/alue (S), maa ja sähköpostiosoite
1. Julkinen avain - Se sisältyy varmenteeseen ja sitä käytetään salaamaan lähetetyt tiedot, jotka puretaan vastaavalla yksityisellä avaimella
1. Tiedot avaimen tyypistä ja pituudesta - Tämä on yleensä RSA 2048, mutta se voi olla myös suurempia kokoja, kuten RSA 4096+

## Viitteet

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)


