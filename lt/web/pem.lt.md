{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEM failas – privatumo padidintas pašto sertifikato failo formatas",
  "description": "Sužinokite apie PEM failo formatą ir API, kurios gali kurti ir atidaryti PEM failus.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-ltm"
}
},
  "lastmod": "2022-09-14"
}

## Kas yra PEM failas?

PEM failas yra saugos sertifikato failas, naudojamas saugiam ryšio kanalui tarp žiniatinklio serverio ir naršyklės sukurti. Jis yra užkoduotas Base64 ir gali turėti privatų raktą, serverio sertifikatą ir (arba) kitų sertifikatų derinį. PEM failai naudojimo požiūriu yra panašūs į .der sertifikatų failus, tačiau saugomi kaip Base64 užkoduotas tekstas, o ne dvejetainiai duomenys. Kiti panašūs sertifikatų failų formatai yra [.cer](/web/cer/) ir [.crt](/web/crt/) failai.

Programos, kurios gali **atidaryti PEM failus**, apima teksto rengykles, tokias kaip Microsoft Notepad ir Apple TextEdit.

## PEM failo formatas

PEM yra konteinerio failo formatas, kuris apibrėžia failo, naudojamo duomenims saugoti, struktūrą ir kodavimo tipą. PEM failai saugomi diske kaip Base64 užkoduotas failo formatas, kurio žmogus neskaito. Standartas apibrėžia, kad PEM failas prasideda taip:

```
-----BEGIN <type>-----
```
ir baigiasi:
```
-----END <type>-----
```

Visas kitas jų turinys yra užkoduotas base64 (didžiosios ir mažosios raidės, skaitmenys, + ir /). Vieną PEM failą gali sudaryti keli blokai, kuriuos gali naudoti kitos programos. Jei PEM faile yra keli sertifikatai, kiekvienas sertifikatas yra atskirtas atskirais blokais taip:

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

### PEM failo pavyzdys

PEM failas su CERTIFICATE bloku paprastai atrodo taip:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

PEM failas su RSA prasideda taip.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Nuorodos Nr.

* [Viešojo rakto kriptografija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kaip sukurti P7C failą?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


