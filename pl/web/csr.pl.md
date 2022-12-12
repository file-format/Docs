{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik CSR - format pliku żądania podpisania certyfikatu",
  "description" :"Dowiedz się, co to jest plik CSR i interfejsy API, które mogą tworzyć i otwierać pliki CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Czym jest plik CSR?

Plik CSR to plik **Żądanie podpisania certyfikatu**, który służy do żądania certyfikatu SSL/TLS. Kiedy potrzebujesz certyfikatu SSL/TLS, generujesz CSR na tym samym serwerze, na którym ostatecznie zostanie zainstalowany. Ten plik CSR jest udostępniany urzędowi certyfikacji (CA) w celu utworzenia certyfikatu. Zawiera informacje, takie jak nazwa zwyczajowa, organizacja, kraj i, co ważniejsze, **klucz publiczny**, który jest zintegrowany z plikiem certyfikatu i jest podpisany odpowiednim kluczem prywatnym.

Aplikacje, które mogą **otwierać pliki CSR**, obejmują OpenSSL i Microsoft IIS.

## Format pliku żądania podpisania certyfikatu

Plik CSR jest tworzony w formacie Base-64 PEM, który można otwierać i przeglądać w prostym edytorze tekstu, takim jak Notatnik firmy Microsoft. Zawiera nagłówek **-----ROZPOCZNIJ WNIOSEK O NOWY CERTYFIKAT-----** na początku pliku i stopkę **-----KONIEC WNIOSEK O NOWY CERTYFIKAT-----** o koniec pliku.

### Jak wygląda plik CSR?

Prosty przykład pliku CSR jest następujący.

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

## Jakie informacje zawiera CSR?

Plik CSR zawiera następujące informacje.

1. „Informacje o firmie i stronie internetowej” — obejmują informacje, takie jak nazwa zwyczajowa, organizacja, jednostka organizacyjna, miasto/lokalizacja, stan/hrabstwo/region (S), kraj i adres e-mail
1. „Klucz publiczny” – jest zawarty w certyfikacie i służy do szyfrowania przesyłanych danych, które są odszyfrowywane przy użyciu odpowiedniego klucza prywatnego
1. „Informacje o typie i długości klucza” — zwykle jest to RSA 2048, ale może też występować w większych rozmiarach, takich jak RSA 4096+

## Bibliografia

* [Serwer aplikacji koncepcyjnych] (https://github.com/Devronium/ConceptApplicationServer)

