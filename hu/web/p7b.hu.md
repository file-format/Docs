{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B – PKCS 7 tanúsítványfájl",
  "description":"További információ a P7C fájlformátumról és az API-król, amelyek P7C fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a P7B fájl?

A P7B fájl egy biztonsági tanúsítványfájl, amely biztonságos digitális tanúsítványt tartalmaz egy személy vagy egy eszköz hitelesítésére. A [.cer](/hu/web/cer/) tanúsítványfájlhoz hasonlóan a P7B fájl is telepíthető a "Tanúsítvány telepítése" opcióval, a fájlra kattintva a jobb gombbal. A P7B a CER fájlformátumtól eltérő formázási lehetőséget használ. Egy vagy több X.509 digitális tanúsítványfájlt tartalmaz, amelyek base64 (ASCII) kódolást használnak. A P7B-fájlokat [ZIP](/hu/compression/zip/) fájlként vagy a tanúsító hatóságtól kapják.

## P7B fájlformátum

A P7B fájlok sima ASCII fájlokként tárolódnak, amelyek bármely szövegszerkesztőben megnyithatók. Tartalmazza a nyilvános kulcsot, amely egy kódolt karakterlánc, amely az olvashatóság szempontjából értelmetlen.

### P7B fájlformátum példa

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenciák ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hogyan hozhatunk létre P7C-fájlt?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

