{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR fails — sertifikāta parakstīšanas pieprasījuma faila formāts",
  "description" : "Uzziniet, kas ir CSR fails un API, kas var izveidot un atvērt CSR failus.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-lv",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Kas ir CSR fails?

CSR fails ir **Certificate Signing Request** fails, ko izmanto, lai pieprasītu SSL/TLS sertifikātu. Kad jums ir nepieciešams SSL/TLS sertifikāts, jūs ģenerējat CSR tajā pašā serverī, kur tas beidzot tiks instalēts. Šis CSR fails tiek koplietots ar sertifikācijas iestādi (CA), lai izveidotu sertifikātu. Tajā ir ietverta tāda informācija kā parastais nosaukums, organizācija, valsts un, vēl svarīgāk, **publiskā atslēga**, kas ir integrēta jūsu sertifikāta failā un ir parakstīta ar atbilstošo privāto atslēgu.

Lietojumprogrammas, kas var **atvērt CSR failus**, ietver OpenSSL un Microsoft IIS.

## Sertifikāta parakstīšanas pieprasījuma faila formāts

CSR fails tiek izveidots Base-64 PEM formātā, ko var atvērt un skatīt vienkāršā teksta redaktorā, piemēram, Microsoft Notepad. Tajā ir iekļauta virsraksts **-----SĀKUMS JAUNS SERTIFIKĀTA PIEPRASĪJUMS-----** faila sākumā un kājene **-----END JAUNS SERTIFIKĀTA PIEPRASĪJUMS-----** plkst. faila beigas.

### Kā izskatās CSR fails?

Vienkāršs CSR faila piemērs ir šāds.

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

## Kāda informācija ir iekļauta CSR?

CSR failā ir šāda informācija.

1. Informācija par uzņēmumu un vietni — ietver tādu informāciju kā vispārpieņemtais nosaukums, organizācija, organizācijas vienība, pilsēta/atrašanās vieta, valsts/apgabals/reģions (S), valsts un e-pasta adrese.
1. Publiskā atslēga — tā ir iekļauta sertifikātā un tiek izmantota, lai šifrētu pārsūtītos datus, kas tiek atšifrēti, izmantojot atbilstošo privāto atslēgu.
1. Informācija par atslēgas veidu un garumu — parasti tas ir RSA 2048, taču var būt arī lielāki izmēri, piemēram, RSA 4096+

## Atsauces

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)


