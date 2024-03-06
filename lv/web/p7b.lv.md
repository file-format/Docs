{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7B — PKCS 7 sertifikāta fails",
  "description": "Uzziniet par P7C faila formātu un API, kas var izveidot un atvērt P7C failus.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-lvb"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir P7B fails?

P7B fails ir drošības sertifikāta fails, kas satur drošu digitālo sertifikātu personas vai ierīces autentifikācijai. Līdzīgi kā [.cer](/web/cer/) sertifikāta failam, P7B failu var instalēt, izmantojot opciju Instalēt sertifikātu, izmantojot peles labo pogu noklikšķiniet uz faila. P7B izmanto citu formatēšanas opciju nekā CER faila formāts. Tajā ir viens vai vairāki X.509 digitālā sertifikāta faili, kas izmanto base64 (ASCII) kodējumu. P7B faili tiek saņemti kā [ZIP](/compression/zip/) fails vai saņemti no sertifikācijas iestādes.

## P7B faila formāts

P7B faili tiek glabāti kā vienkārši ASCII faili, kurus var atvērt jebkurā teksta redaktorā. Tā satur publisko atslēgu, kas ir kodēta virkne, kas no lasāmības viedokļa ir bezjēdzīga.

### P7B faila formāta piemērs

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Atsauces Nr.

* [Publiskās atslēgas kriptogrāfija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kā izveidot P7C failu?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


