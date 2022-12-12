{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Fișier de certificat PKCS 7",
  "description":"Aflați despre formatul de fișier P7C și despre API-urile care pot crea și deschide fișiere P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier P7B?

Un fișier P7B este un fișier cu certificat de securitate care conține un certificat digital securizat pentru autentificarea unei persoane sau a unui dispozitiv. Similar cu un fișier de certificat [.cer](/ro/web/cer/), un fișier P7B poate fi instalat folosind opțiunea „Instalare certificat” folosind opțiunea de clic dreapta pe fișier. P7B utilizează o opțiune de formatare diferită decât formatul de fișier CER. Conține unul sau mai multe fișiere de certificat digital X.509 care utilizează codificarea base64 (ASCII). Fișierele P7B sunt primite ca fișier [ZIP](/ro/compression/zip/) sau primite de la autoritatea de certificare.

## Format de fișier P7B

Fișierele P7B sunt stocate ca fișiere ASCII simple care pot fi deschise în orice editor de text. Conține cheia publică care este un șir codificat care este lipsit de sens din punctul de vedere al lizibilității.

### Exemplu de format de fișier P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referințe ##

* [Public Key Criptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Cum se creează fișierul P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

