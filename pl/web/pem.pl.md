{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik PEM — format pliku certyfikatu poczty o zwiększonej prywatności",
  "description":"Poznaj format pliku PEM i interfejsy API, które mogą tworzyć i otwierać pliki PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Czym jest plik PEM?

Plik PEM to plik certyfikatu bezpieczeństwa, który służy do ustanowienia bezpiecznego kanału komunikacyjnego między serwerem WWW a przeglądarką. Jest zakodowany w standardzie Base64 i może zawierać klucz prywatny, certyfikat serwera i/lub kombinację innych certyfikatów. Pliki PEM są podobne do plików certyfikatów .der pod względem użytkowania, ale są przechowywane jako tekst zakodowany w formacie Base64, a nie jako dane binarne. Inne podobne formaty plików certyfikatów obejmują pliki [.cer](/pl/web/cer/) i [.crt](/pl/web/crt/).

Aplikacje, które mogą **otwierać pliki PEM**, obejmują edytory tekstu, takie jak Microsoft Notepad i Apple TextEdit.

## Format pliku PEM

PEM to format pliku kontenera, który definiuje strukturę i typ kodowania pliku używanego do przechowywania danych. Pliki PEM są zapisywane na dysku jako format pliku zakodowany w formacie Base64, który nie jest czytelny dla człowieka. Norma określa, że plik PEM zaczyna się od:

```
-----BEGIN <type>-----
```
i kończy się na:
```
-----END <type>-----
```

Cała pozostała zawartość w nich jest zakodowana base64 (wielkie i małe litery, cyfry, + i /). Pojedynczy plik PEM może składać się z wielu bloków, z których mogą korzystać inne programy. Jeśli plik PEM zawiera wiele certyfikatów, każdy certyfikat jest oddzielony oddzielnymi blokami w następujący sposób:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Przykład pliku PEM

Plik PEM z blokiem CERTIFICATE zwykle wygląda następująco:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Plik PEM z RSA zaczyna się jak poniżej.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Bibliografia ##

* [Kryptografia klucza publicznego](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak utworzyć plik P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

