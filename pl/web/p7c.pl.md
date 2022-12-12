{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Plik Certyfikatu PKCS 7",
  "description":"Poznaj format pliku P7C i interfejsy API, które mogą tworzyć i otwierać pliki P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik P7C?

Plik P7C, podobnie jak inne pliki certyfikatów bezpieczeństwa, jest cyfrowym certyfikatem używanym do uwierzytelniania tożsamości w sieci. Aplikacje korzystające z certyfikatów uwierzytelniają tożsamość przy użyciu klucza publicznego zawartego w tych plikach certyfikatów. Kryptografia z kluczem publicznym lub kryptografia asymetryczna wykorzystuje parę kluczy, z których jeden jest kluczem publicznym, a drugi jest znany jako klucz prywatny. Klucz prywatny jest przechowywany w bezpiecznym miejscu, aby zapewnić skuteczną ochronę, podczas gdy klucz publiczny można udostępniać innym osobom. Inne popularne formaty plików certyfikatów to [CRT](/pl/web/crt/), DER i PEM.

## Format pliku P7C — więcej informacji

Pliki P7C są zapisywane na dysku jako pliki binarne i zawierają informacje o kluczu publicznym wygenerowane przy użyciu algorytmów kryptograficznych opartych na problemach matematycznych. Można je otworzyć w dowolnym edytorze tekstu, ale ich zawartość nie jest w formie czytelnej dla człowieka. Niektóre aplikacje, które mogą otwierać pliki P7C, to Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager i Microsoft Windows Contacts.

### Przykład formatu pliku P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Bibliografia ##

* [Kryptografia klucza publicznego](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak utworzyć plik P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

