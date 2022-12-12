{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku KEY i interfejsy API, które mogą tworzyć i otwierać pliki KEY.",
  "title" :"Format pliku klucza — plik klucza prywatnego poczty o zwiększonej prywatności",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Czym jest plik KEY?

Plik KEY to prywatna część mechanizmu bezpieczeństwa zapisana na dysku w formacie pliku Privacy-Enhanced Mal (PEM). Służy do odszyfrowywania informacji wymienianych między przeglądarką internetową a serwerem WWW obsługującym żądania przeglądania. Plik KEY zawiera zakodowane ciągi znaków, które są bezużyteczne dla ludzkiego oka, ale stanowią istotę szyfrowania/odszyfrowywania wymiany informacji w ramach certyfikatu SSL na serwerach WWW. Pliki KEY są generowane automatycznie i instalowane po stronie klienta.

Pliki **KEY** można otwierać za pomocą dowolnego edytora tekstu, takiego jak Microsoft Notepad (Windows), Apple TextEdit (Mac) lub GitHub Atom (międzyplatformowy). Pliki KEY są podobne do formatów plików [CRT](/pl/web/crt/) i [CER](/pl/web/cer/).

## KEY Format pliku — więcej informacji

Pliki KEY są przechowywane na dysku jako zwykłe pliki tekstowe, ale są to zakodowane ciągi znaków, które nie są przyjazne dla człowieka do odczytania. Praktycznie użytkownicy nie rozumieją ciągów znaków po otwarciu w edytorze tekstu. Certyfikat klucza prywatnego jest poufny i nie należy go nikomu udostępniać. Cały proces zabezpieczania wymiany informacji w Internecie obejmuje:

* **Klucz publiczny** - używany do szyfrowania informacji o użytkowniku w celu wymiany danych między przeglądarką a serwerami WWW
* **Klucz prywatny** - używany do odszyfrowywania informacji otrzymywanych przez serwer WWW

Certyfikaty SSL, znane również jako certyfikaty X.509, są unikalne dla każdej witryny. KEY przy użyciu następującej składni:

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

### Przykład pliku klucza

Poniżej znajduje się przykład pliku klucza prywatnego.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Bibliografia

* [Klucze publiczne, klucze prywatne i certyfikaty](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

