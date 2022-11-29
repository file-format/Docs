{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR-fil - filformat för begäran om certifikatsignering",
  "description" :"Läs mer om vad en CSR-fil och API:er är som kan skapa och öppna CSR-filer.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Vad är en CSR fil?

En CSR-fil är en **Certificate Signing Request**-fil som används för att begära SSL/TLS-certifikat. När du behöver ha ditt SSL/TLS-certifikat genererar du CSR på samma server där det slutligen ska installeras. Denna CSR-fil delas med certifikatutfärdaren (CA) för att skapa certifikatet. Den innehåller information som vanligt namn, organisation, land och, ännu viktigare, den **offentliga nyckeln** som är integrerad i din certifikatfil och är signerad med motsvarande privata nyckel.

Applikationer som kan **öppna CSR-filer** inkluderar OpenSSL och Microsoft IIS.

## Filformat för begäran om certifikatsignering

En CSR-fil skapas i ett Base-64 PEM-format som kan öppnas och visas i en enkel textredigerare som Microsoft Notepad. Den innehåller en rubrik **-----BÖRJAN NY BEGÄRAN AV CERTIFIKAT-----** i början av filen och en sidfot **-----SLUT NYTT CERTIFIKAT BEGÄRAN-----** kl. slutet av filen.

### Hur ser en CSR-fil ut?

Ett enkelt exempel på en CSR-fil är följande.

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

## Vilken information ingår i en CSR?

En CSR-fil innehåller följande information.

1. "Information om företag och webbplats" - Innehåller information som vanligt namn, organisation, organisationsenhet, stad/ort, stat/län/region (S), land och e-postadress
1. "Public Key" - Den ingår i certifikatet och används för att kryptera överförda data som dekrypteras med motsvarande privata nyckel
1. `Information om nyckeltyp och längd` - Detta är vanligtvis RSA 2048 men kan även komma i större storlekar som RSA 4096+

## Referenser

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

