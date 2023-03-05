{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл CSR — формат файла запроса на подпись сертификата",
  "description" :"Узнайте, что такое файл CSR и API, которые могут создавать и открывать файлы CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## .CSR вариант №

Файл CSR — это файл **Запроса на подпись сертификата**, который используется для запроса сертификата SSL/TLS. Когда вам нужен сертификат SSL/TLS, вы создаете CSR на том же сервере, где он будет окончательно установлен. Этот файл CSR передается Центру сертификации (ЦС) для создания сертификата. Он содержит такую информацию, как обычное имя, организация, страна и, что более важно, **открытый ключ**, который интегрирован в ваш файл сертификата и подписан соответствующим закрытым ключом.

Приложения, которые могут **открывать файлы CSR**, включают OpenSSL и Microsoft IIS.

## Формат файла запроса на подпись сертификата

Файл CSR создается в формате PEM Base-64, который можно открыть и просмотреть в простом текстовом редакторе, таком как Блокнот Microsoft. Он включает заголовок **-----BEGIN NEW CERTIFICATE REQUEST-----** в начале файла и нижний колонтитул **-----END NEW CERTIFICATE REQUEST-----** в конец файла.

### Как выглядит файл CSR?

Ниже приведен простой пример файла CSR.

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

## Какая информация содержится в CSR?

Файл CSR содержит следующую информацию.

1. «Информация о бизнесе и веб-сайте» — включает такую информацию, как обычное имя, организация, организационная единица, город/населенный пункт, штат/округ/регион (S), страна и адрес электронной почты.
1. «Открытый ключ» — он включен в сертификат и используется для шифрования передаваемых данных, которые расшифровываются с использованием соответствующего закрытого ключа.
1. «Информация о типе и длине ключа». Обычно это RSA 2048, но могут быть и большие размеры, например RSA 4096+.

## использованная литература

* [Сервер концептуальных приложений](https://github.com/Devronium/ConceptApplicationServer)

