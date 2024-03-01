{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7B - PKCS 7 -sertifikaattitiedosto",
  "description": "Opi P7C-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata P7C-tiedostoja.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-fib"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on P7B-tiedosto?

P7B-tiedosto on suojaussertifikaattitiedosto, joka sisältää suojatun digitaalisen sertifikaatin henkilön tai laitteen todentamiseen. Kuten [.cer](/web/cer/)-varmennetiedosto, P7B-tiedosto voidaan asentaa käyttämällä Asenna varmenne -vaihtoehtoa napsauttamalla tiedostoa hiiren kakkospainikkeella. P7B käyttää eri muotoiluvaihtoehtoa kuin CER-tiedostomuoto. Se sisältää vähintään yhden X.509-digitaalisen varmennetiedoston, joka käyttää base64 (ASCII) -koodausta. P7B-tiedostot vastaanotetaan [ZIP](/compression/zip/)-tiedostona tai varmenteen myöntäjältä.

## P7B tiedostomuoto

P7B-tiedostot tallennetaan tavallisina ASCII-tiedostoina, jotka voidaan avata missä tahansa tekstieditorissa. Se sisältää julkisen avaimen, joka on koodattu merkkijono, joka on luettavuuden kannalta merkityksetön.

### Esimerkki P7B-tiedostomuodosta

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Viitteet ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kuinka luodaan P7C-tiedosto?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


