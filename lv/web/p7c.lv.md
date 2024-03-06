{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7C — PKCS 7 sertifikāta fails",
  "description": "Uzziniet par P7C faila formātu un API, kas var izveidot un atvērt P7C failus.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-lvc"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir P7C fails?

P7C fails, tāpat kā citi drošības sertifikātu faili, ir digitālais sertifikāts, ko izmanto identitātes autentificēšanai tīklā. Programmas, kas izmanto sertifikātus, autentificē identitāti, izmantojot publisko atslēgu, kas iekļauta šajos sertifikātu failos. Publiskās atslēgas kriptogrāfija jeb asimetriskā kriptogrāfija izmanto atslēgu pāri, no kuriem viena ir publiskā atslēga, bet otra ir pazīstama kā privātā atslēga. Privātā atslēga tiek turēta drošībā efektīvai drošībai, savukārt publisko atslēgu var koplietot ar citiem. Citi izplatīti sertifikātu failu formāti ir [CRT](/web/crt/), DER un PEM.

## P7C faila formāts — vairāk informācijas

P7C faili tiek saglabāti diskā kā bināri faili, un tajos ir iekļauta publiskās atslēgas informācija, kas ģenerēta, izmantojot kriptogrāfiskus algoritmus, kuru pamatā ir matemātiskas problēmas. Tos var atvērt jebkurā teksta redaktorā, taču to saturs nav cilvēkiem lasāmā formā. Dažas lietojumprogrammas, kas var atvērt P7C failus, ir Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager un Microsoft Windows Contacts.

### P7C faila formāta piemērs

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Atsauces Nr.

* [Publiskās atslēgas kriptogrāfija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kā izveidot P7C failu?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


