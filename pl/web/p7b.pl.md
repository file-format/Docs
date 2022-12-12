{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Plik Certyfikatu PKCS 7",
  "description":"Poznaj format pliku P7C i interfejsy API, które mogą tworzyć i otwierać pliki P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik P7B?

Plik P7B to plik certyfikatu bezpieczeństwa, który zawiera bezpieczny certyfikat cyfrowy do uwierzytelniania osoby lub urządzenia. Podobnie jak w przypadku pliku certyfikatu [.cer](/pl/web/cer/), plik P7B można zainstalować przy użyciu opcji „Zainstaluj certyfikat”, klikając plik prawym przyciskiem myszy. P7B używa innej opcji formatowania niż format pliku CER. Zawiera co najmniej jeden plik certyfikatu cyfrowego X.509 korzystający z kodowania base64 (ASCII). Pliki P7B są odbierane jako plik [ZIP](/pl/compression/zip/) lub odbierane z urzędu certyfikacji.

## Format pliku P7B

Pliki P7B są przechowywane jako zwykłe pliki ASCII, które można otworzyć w dowolnym edytorze tekstu. Zawiera klucz publiczny, który jest zakodowanym ciągiem znaków, który jest bez znaczenia z punktu widzenia czytelności.

### Przykład formatu pliku P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Bibliografia ##

* [Kryptografia klucza publicznego](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak utworzyć plik P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

