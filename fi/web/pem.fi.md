{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEM-tiedosto - Tietosuoja Enhanced Mail Certificate -tiedostomuoto",
  "description": "Opi PEM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PEM-tiedostoja.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-fim"
}
},
  "lastmod": "2022-09-14"
}

## Mikä on PEM-tiedosto?

PEM-tiedosto on suojaussertifikaattitiedosto, jota käytetään luomaan suojattu viestintäkanava verkkopalvelimen ja selaimen välille. Se on Base64-koodattu ja voi sisältää yksityisen avaimen, palvelinvarmenteen ja/tai yhdistelmän muita varmenteita. PEM-tiedostot ovat käytön suhteen samanlaisia kuin .der-sertifikaattitiedostot, mutta ne tallennetaan Base64-koodatuksi tekstiksi binääritietojen sijaan. Muita samanlaisia varmennetiedostomuotoja ovat tiedostot [.cer](/web/cer/) ja [.crt](/web/crt/).

Sovelluksia, jotka voivat **avata PEM-tiedostoja**, ovat tekstieditorit, kuten Microsoft Notepad ja Apple TextEdit.

## PEM-tiedostomuoto

PEM on säilötiedostomuoto, joka määrittää tietojen tallentamiseen käytettävän tiedoston rakenteen ja koodaustyypin. PEM-tiedostot tallennetaan levylle Base64-koodatussa tiedostomuodossa, joka ei ole ihmisen luettavissa. Standardi määrittelee, että PEM-tiedosto alkaa seuraavasti:

```
-----BEGIN <type>-----
```
ja päättyy:
```
-----END <type>-----
```

Kaikki muu sisältö näiden sisällä on base64-koodattua (isot ja pienet kirjaimet, numerot, + ja /). Yksi PEM-tiedosto voi sisältää useita lohkoja, joita muut ohjelmat voivat käyttää. Jos PEM-tiedosto sisältää useita varmenteita, kukin varmenne erotetaan yksittäisillä lohkoilla seuraavasti:

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

### PEM-tiedostoesimerkki

CERTIFICATE-lohkolla varustettu PEM-tiedosto näyttää yleensä tältä:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

PEM-tiedosto RSA:lla alkaa seuraavasti.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Viitteet ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kuinka luodaan P7C-tiedosto?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


