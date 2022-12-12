{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier CSR - Format fișier de cerere de semnare a certificatului",
  "description" :"Aflați despre ce este un fișier CSR și API-urile care pot crea și deschide fișiere CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Ce este un fișier CSR?

Un fișier CSR este un fișier **Solicitare de semnare a certificatului** care este utilizat pentru a solicita un certificat SSL/TLS. Când trebuie să aveți certificatul SSL/TLS, generați CSR-ul pe același server unde va fi instalat în cele din urmă. Acest fișier CSR este partajat cu Autoritatea de Certificare (CA) pentru crearea certificatului. Conține informații precum numele comun, organizația, țara și, mai important, **cheia publică** care este integrată în fișierul dvs. de certificat și este semnată cu cheia privată corespunzătoare.

Aplicațiile care pot **deschide fișierele CSR** includ OpenSSL și Microsoft IIS.

## Format de fișier pentru cererea de semnare a certificatului

Un fișier CSR este creat într-un format Base-64 PEM care poate fi deschis și vizualizat într-un editor de text simplu, cum ar fi Microsoft Notepad. Include un antet **-----ÎNCEPE CERERE DE CERTIFICAT NOU-----** la începutul fișierului și un subsol **-----ÎNCEPE CERERE DE CERTIFICAT NOU-----** la sfârşitul dosarului.

### Cum arată un fișier CSR?

Un exemplu simplu de fișier CSR este următorul.

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

## Ce informații sunt incluse într-un CSR?

Un fișier CSR conține următoarele informații.

1. „Informații despre companie și site web” - Include informații precum numele comun, organizația, unitatea organizațională, orașul/localitatea, statul/județul/regiunea (S), țara și adresa de e-mail
1. `Cheie publică` - Este inclusă în certificat și este folosită pentru a cripta datele transmise, care sunt decriptate folosind cheia privată corespunzătoare
1. „Informații despre tipul și lungimea cheii” - Acesta este de obicei RSA 2048, dar poate veni și în dimensiuni mai mari, cum ar fi RSA 4096+

## Referințe

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

