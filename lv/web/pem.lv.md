{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEM fails — pasta sertifikāta faila formāts ar uzlabotu konfidencialitāti",
  "description": "Uzziniet par PEM faila formātu un API, kas var izveidot un atvērt PEM failus.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-lvm"
}
},
  "lastmod": "2022-09-14"
}

## Kas ir PEM fails?

PEM fails ir drošības sertifikāta fails, ko izmanto, lai izveidotu drošu saziņas kanālu starp tīmekļa serveri un pārlūkprogrammu. Tas ir Base64 kodēts un var saturēt privāto atslēgu, servera sertifikātu un/vai citu sertifikātu kombināciju. PEM faili lietojuma ziņā ir līdzīgi .der sertifikātu failiem, taču tie tiek glabāti kā Base64 kodēts teksts, nevis bināri dati. Citi līdzīgi sertifikātu failu formāti ietver [.cer](/web/cer/) un [.crt](/web/crt/) failus.

Lietojumprogrammas, kas var **atvērt PEM failus**, ietver teksta redaktorus, piemēram, Microsoft Notepad un Apple TextEdit.

## PEM faila formāts

PEM ir konteinera faila formāts, kas nosaka datu glabāšanai izmantotā faila struktūru un kodējuma veidu. PEM faili tiek saglabāti diskā Base64 kodētā faila formātā, kas nav cilvēkiem lasāms. Standarts nosaka, ka PEM fails sākas ar:

```
-----BEGIN <type>-----
```
un beidzas ar:
```
-----END <type>-----
```

Viss pārējais saturs tajos ir kodēts base64 (lielie un mazie burti, cipari, + un /). Viens PEM fails var sastāvēt no vairākiem blokiem, kurus var izmantot citas programmas. Ja PEM failā ir vairāki sertifikāti, katrs sertifikāts tiek atdalīts ar atsevišķiem blokiem šādi:

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

### PEM faila piemērs

PEM fails ar CERTIFICATE bloku parasti izskatās šādi:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

PEM fails ar RSA sākas šādi.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Atsauces Nr.

* [Publiskās atslēgas kriptogrāfija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kā izveidot P7C failu?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


