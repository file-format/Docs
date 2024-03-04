{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7C – PKCS 7 sertifikato failas",
  "description": "Sužinokite apie P7C failo formatą ir API, kurios gali kurti ir atidaryti P7C failus.",
  "linktitle": "P7C",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-p7-ltc"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra P7C failas?

P7C failas, kaip ir kiti saugos sertifikato failai, yra skaitmeninis sertifikatas, naudojamas tapatybei tinkle patvirtinti. Sertifikatus naudojančios programos tapatybę patvirtina naudodamos viešąjį raktą, įtrauktą į šiuos sertifikatų failus. Viešojo rakto kriptografija arba asimetrinė kriptografija naudoja raktų porą, iš kurių vienas yra viešasis raktas, o kitas yra žinomas kaip privatus raktas. Privatusis raktas yra saugomas siekiant efektyvaus saugumo, o viešasis raktas gali būti bendrinamas su kitais. Kiti įprasti sertifikatų failų formatai yra [CRT](/web/crt/), DER ir PEM.

## P7C failo formatas – daugiau informacijos

P7C failai išsaugomi diske kaip dvejetainiai failai ir apima viešojo rakto informaciją, sugeneruotą naudojant kriptografinius algoritmus, pagrįstus matematinėmis problemomis. Juos galima atidaryti bet kuriame teksto rengyklėje, tačiau jų turinys nėra žmonėms suprantama forma. Kai kurios programos, kurios gali atidaryti P7C failus, yra Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager ir Microsoft Windows Contacts.

### P7C failo formato pavyzdys

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Nuorodos Nr.

* [Viešojo rakto kriptografija](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Kaip sukurti P7C failą?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


