{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CSR failas – sertifikato pasirašymo užklausos failo formatas",
  "description" : "Sužinokite, kas yra CSR failas ir API, kurios gali kurti ir atidaryti CSR failus.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-lt",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Kas yra CSR failas?

CSR failas yra **Sertifikato pasirašymo užklausos** failas, naudojamas SSL/TLS sertifikato užklausai pateikti. Kai reikia turėti SSL/TLS sertifikatą, CSR sugeneruosite tame pačiame serveryje, kuriame jis pagaliau bus įdiegtas. Šis CSR failas yra bendrinamas su sertifikato institucija (CA), kad būtų sukurtas sertifikatas. Jame yra tokia informacija kaip įprastas pavadinimas, organizacija, šalis ir, dar svarbiau, **viešasis raktas**, kuris yra integruotas į jūsų sertifikato failą ir yra pasirašytas atitinkamu privačiu raktu.

Programos, kurios gali **atidaryti CSR failus**, apima OpenSSL ir Microsoft IIS.

## Sertifikato pasirašymo užklausos failo formatas

CSR failas sukuriamas Base-64 PEM formatu, kurį galima atidaryti ir peržiūrėti naudojant paprastą teksto rengyklę, pvz., Microsoft Notepad. Failo pradžioje yra antraštė **-----PRADĖJIMAS NAUJO SERTIFIKATO PRAŠYMAS-----** ir poraštė **-------------** failo pabaiga.

### Kaip atrodo CSR failas?

Paprastas CSR failo pavyzdys yra toks.

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

## Kokia informacija įtraukta į CSR?

CSR faile yra ši informacija.

1. Informacija apie verslą ir svetainę – apima tokią informaciją kaip bendras pavadinimas, organizacija, organizacinis vienetas, miestas / vietovė, valstija / apskritis / regionas (S), šalis ir el. pašto adresas
1. Viešasis raktas – jis įtrauktas į sertifikatą ir naudojamas perduodamiems duomenims užšifruoti, kurie iššifruojami naudojant atitinkamą privatų raktą.
1. Informacija apie rakto tipą ir ilgį – paprastai tai yra RSA 2048, bet gali būti ir didesnių dydžių, pvz., RSA 4096+

## Nuorodos

* [Concept Application Server] (https://github.com/Devronium/ConceptApplicationServer)


