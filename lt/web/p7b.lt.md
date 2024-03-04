{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7B – PKCS 7 sertifikato failas",
  "description": "Sužinokite apie P7C failo formatą ir API, kurios gali kurti ir atidaryti P7C failus.",
  "linktitle": "P7B",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-ltb"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra P7B failas?

P7B failas yra saugos sertifikato failas, kuriame yra saugus skaitmeninis sertifikatas, skirtas asmens ar įrenginio autentifikavimui. Panašiai kaip [.cer](/web/cer/) sertifikato failas, P7B failas gali būti įdiegtas naudojant parinktį Įdiegti sertifikatą, dešiniuoju pelės mygtuku spustelėjus failą. P7B naudoja kitokią formatavimo parinktį nei CER failo formatas. Jame yra vienas ar daugiau X.509 skaitmeninių sertifikatų failų, kuriuose naudojama base64 (ASCII) koduotė. P7B failai gaunami kaip [ZIP](/compression/zip/) failas arba gauti iš sertifikatų institucijos.

## P7B failo formatas

P7B failai saugomi kaip paprasti ASCII failai, kuriuos galima atidaryti bet kuriame teksto rengyklėje. Jame yra viešasis raktas, kuris yra užkoduota eilutė, kuri skaitomumo požiūriu yra beprasmė.

### P7B failo formato pavyzdys

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Nuorodos Nr.

* [Viešojo rakto kriptografija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kaip sukurti P7C failą?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


