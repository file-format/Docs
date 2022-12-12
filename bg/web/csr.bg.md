{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR файл – Файлов формат за заявка за подписване на сертификат",
  "description" :"Научете какво е CSR файл и API, които могат да създават и отварят CSR файлове.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Какво е CSR файл?

CSR файлът е **Certificate Signing Request** файл, който се използва за заявка за SSL/TLS сертификат. Когато трябва да имате своя SSL/TLS сертификат, вие генерирате CSR на същия сървър, където най-накрая ще бъде инсталиран. Този CSR файл се споделя със Сертифициращия орган (CA) за създаване на сертификата. Той съдържа информация като общо име, организация, държава и, което е по-важно, **публичния ключ**, който е интегриран във вашия сертификатен файл и е подписан със съответния частен ключ.

Приложенията, които могат да **отварят CSR файлове** включват OpenSSL и Microsoft IIS.

## Файлов формат на заявка за подписване на сертификат

CSR файл се създава във формат Base-64 PEM, който може да се отваря и разглежда в прост текстов редактор като Microsoft Notepad. Той включва заглавка **-----НАЧАЛО НА ЗАЯВКА ЗА НОВ СЕРТИФИКАТ-----** в началото на файла и долен колонтитул **-----КРАЙ НА ЗАЯВКА ЗА НОВ СЕРТИФИКАТ-----** в края на файла.

### Как изглежда CSR файл?

Прост пример за CSR файл е както следва.

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

## Каква информация е включена в CSR?

CSR файл съдържа следната информация.

1. `Информация за бизнеса и уебсайта` - Включва информация като общо име, организация, организационна единица, град/населено място, щат/окръг/регион (S), държава и имейл адрес
1. `Публичен ключ` - Той е включен в сертификата и се използва за криптиране на предадени данни, които се дешифрират с помощта на съответния частен ключ
1. „Информация за типа и дължината на ключа“ – Това обикновено е RSA 2048, но може да се предлага и в по-големи размери като RSA 4096+

## Препратки

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

