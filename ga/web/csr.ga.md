{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad CSR - Formáid an Chomhaid Iarratais do Shíniú Teastais",
  "description" : "Foghlaim faoi cad is comhad CSR agus APIs ann ar féidir comhaid CSR a chruthú agus a oscailt.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-ga",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Cad is comhad CSR ann?

Is comhad **Iarratas ar Shíniú Teastais** é comhad CSR a úsáidtear chun teastas SSL/TLS a iarraidh. Nuair is gá duit do theastas SSL/TLS a bheith agat, gineann tú an CSR ar an bhfreastalaí céanna áit a mbeidh sé suiteáilte ar deireadh. Roinntear an comhad CSR seo leis an Údarás Deimhniúcháin (CA) chun an deimhniú a chruthú. Tá faisnéis ann mar ainm coitianta, eagraíocht, tír, agus, níos tábhachtaí fós, an **eochair phoiblí** atá comhtháite laistigh de do chomhad teastais agus atá sínithe leis an eochair phríobháideach chomhfhreagrach.

I measc na n-iarratas ar féidir **comhaid CSR a oscailt** tá OpenSSL agus Microsoft IIS.

## Formáid Chomhaid Iarratais do Shíniú Teastais

Cruthaítear comhad CSR i bhformáid Base-64 PEM is féidir a oscailt agus a fheiceáil in eagarthóir téacs simplí ar nós Microsoft Notepad. Áiríonn sé ceanntásc **----- IARRATAS AR AN TEASTAIS NUA -----** ag tús an chomhaid agus buntásc **----- DEIREADH IARRATAS AR THEASTAIS -----** ag deireadh an chomhaid.

### Conas atá comhad CSR?

Seo a leanas sampla simplí de chomhad CSR.

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

## Cén fhaisnéis atá san áireamh i CSR?

Tá an fhaisnéis seo a leanas i gcomhad CSR.

1. `Faisnéis faoi Ghnó agus Suíomh Gréasáin` - Áirítear leis sin faisnéis amhail Ainm Coiteann, Eagraíocht, Aonad Eagrúcháin, Cathair/Ceantar, Stát/Contae/Réigiún (S), Tír agus Seoladh Ríomhphoist
1. `Eochair Phoiblí` - Tá sé san áireamh sa teastas agus úsáidtear é chun sonraí a tharchuirtear a chriptiú a dhíchriptítear leis an eochair phríobháideach chomhfhreagrach
1. `Faisnéis faoi Phríomhchineál agus Fad` - Is gnách gurb é seo RSA 2048 ach d'fhéadfadh sé teacht i méideanna níos mó mar RSA 4096+

## Tagairtí

* [Freastalaí Feidhmchláir Coincheap]( https://github.com/Devronium/ConceptApplicationServer)


