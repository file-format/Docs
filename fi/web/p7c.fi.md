{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7C - PKCS 7 -sertifikaattitiedosto",
  "description": "Opi P7C-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata P7C-tiedostoja.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-fic"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on P7C-tiedosto?

P7C-tiedosto, kuten muutkin suojaussertifikaattitiedostot, on digitaalinen varmenne, jota käytetään henkilöllisyyden todentamiseen verkossa. Varmenteita käyttävät sovellukset todentavat henkilöllisyyden käyttämällä näihin varmennetiedostoihin sisältyvää julkista avainta. Julkisen avaimen salakirjoitus tai epäsymmetrinen salaus käyttää avaimia, joista toinen on julkinen avain ja toinen tunnetaan yksityisenä avaimena. Yksityinen avain pidetään suojattuna tehokkaan turvallisuuden takaamiseksi, kun taas julkinen avain voidaan jakaa muiden kanssa. Muita yleisiä varmennetiedostomuotoja ovat [CRT](/web/crt/), DER ja PEM.

## P7C-tiedostomuoto - lisätietoja

P7C-tiedostot tallennetaan levylle binääritiedostoina ja sisältävät julkisen avaimen tiedot, jotka on luotu matemaattisiin ongelmiin perustuvilla salausalgoritmeilla. Ne voidaan avata millä tahansa tekstieditorilla, mutta niiden sisältö ei ole ihmisen luettavassa muodossa. Joitakin sovelluksia, jotka voivat avata P7C-tiedostoja, ovat Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager ja Microsoft Windows Contacts.

### Esimerkki P7C-tiedostomuodosta

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Viitteet ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kuinka luodaan P7C-tiedosto?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


