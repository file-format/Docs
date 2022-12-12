{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл CSR – формат файлу запиту на підписання сертифіката",
  "description" :"Дізнайтеся, що таке файл CSR та API, які можуть створювати та відкривати файли CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Що таке файл CSR?

Файл CSR — це файл **запиту на підписання сертифіката**, який використовується для запиту сертифіката SSL/TLS. Коли вам потрібен сертифікат SSL/TLS, ви генеруєте CSR на тому самому сервері, де його буде остаточно встановлено. Цей файл CSR надається спільно з центром сертифікації (CA) для створення сертифіката. Він містить таку інформацію, як загальна назва, організація, країна та, що більш важливо, **відкритий ключ**, який інтегровано у ваш файл сертифіката та підписаний відповідним закритим ключем.

Програми, які можуть **відкривати файли CSR**, включають OpenSSL і Microsoft IIS.

## Формат файлу запиту на підписання сертифіката

Файл CSR створюється у форматі Base-64 PEM, який можна відкрити та переглянути в простому текстовому редакторі, наприклад Microsoft Notepad. Він містить заголовок **-----ПОЧАТИ НОВИЙ ЗАПИТ СЕРТИФІКАТУ-----** на початку файлу та нижній колонтитул **-----КІНЕЦЬ НОВИЙ ЗАПИТУ СЕРТИФІКАТУ-----** на кінець файлу.

### Як виглядає файл CSR?

Нижче наведено простий приклад файлу CSR.

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

## Яка інформація міститься в CSR?

Файл CSR містить таку інформацію.

1. «Інформація про компанію та веб-сайт» – містить таку інформацію, як загальна назва, організація, організаційний підрозділ, місто/населений пункт, штат/округ/регіон (S), країна та електронна адреса
1. `Відкритий ключ` - він включений у сертифікат і використовується для шифрування переданих даних, які розшифровуються за допомогою відповідного закритого ключа
1. `Інформація про тип і довжину ключа` - зазвичай це RSA 2048, але також може надходити у більших розмірах, наприклад RSA 4096+

## Список літератури

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

