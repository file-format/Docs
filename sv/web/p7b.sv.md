{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 certifikatfil",
  "description":"Läs mer om P7C-filformat och API:er som kan skapa och öppna P7C-filer.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är P7B fil?

En P7B-fil är en säkerhetscertifikatfil som innehåller ett säkert digitalt certifikat för autentisering av en person eller enhet. På samma sätt som en [.cer](/sv/web/cer/) certifikatfil kan en P7B-fil installeras med alternativet "Installera certifikat" genom att använda högerklicksalternativet på filen. P7B använder ett annat formateringsalternativ än CER-filformatet. Den innehåller en eller flera X.509 digitala certifikatfiler som använder base64 (ASCII)-kodning. P7B-filer tas emot som en [ZIP](/sv/compression/zip/)-fil eller tas emot från certifikatutfärdare.

## P7B filformat

P7B-filer lagras som vanliga ASCII-filer som kan öppnas i vilken textredigerare som helst. Den innehåller den publika nyckeln som är en kodad sträng som är meningslös ur läsbarhetssynpunkt.

### P7B Filformat Exempel

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenser ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hur skapar jag P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

