{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "plik crt", "format pliku crt", "typ pliku crt", "plik", "typ", "co to jest plik crt"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - format pliku certyfikatu bezpieczeństwa",
  "description":"Poznaj format pliku CRT i interfejsy API, które mogą tworzyć i otwierać pliki CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik CRT?

Plik z rozszerzeniem .crt to plik certyfikatu bezpieczeństwa używany przez bezpieczne strony internetowe do nawiązywania bezpiecznych połączeń z serwera WWW do przeglądarki. Bezpieczne strony internetowe umożliwiają bezpieczne przesyłanie danych, logowanie, transakcje kartą płatniczą oraz zapewniają bezpieczne przeglądanie strony. Jeśli otworzysz bezpieczną witrynę, na pasku adresu zobaczysz ikonę kłódki. Jeśli go klikniesz, możesz wyświetlić szczegóły zainstalowanego certyfikatu. Międzynarodowe firmy, takie jak Verisign i Thawte, dystrybuują te certyfikaty SSL.

## Format pliku CRT

Pliki CRT są w formacie ASCII i można je otworzyć w dowolnym edytorze tekstu, aby wyświetlić zawartość pliku certyfikatu. Jest zgodny ze standardem certyfikacji X.509, który definiuje strukturę certyfikatu. Określa pola danych, które powinny znaleźć się w certyfikacie SSL. CRT należy do formatu PEM certyfikatów, które są plikami zakodowanymi w Base64 ASCII.

### Struktura pliku PEM

Plik PEM może mieć wiele certyfikatów. W takim przypadku każdy certyfikat w pliku PEM ma następującą strukturę.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Przykład formatu pliku CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Bibliografia ##

* [Klucze publiczne, klucze prywatne i certyfikaty](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

