{
  "date": "2022-09-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEM-fil - Privatlivsforbedret postcertifikatfilformat",
  "description": "Lær om PEM-filformat og API'er, der kan oprette og åbne PEM-filer.",
  "linktitle": "PEM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pe-dam"
}
},
  "lastmod": "2022-09-14"
}

## Hvad er en PEM fil?

En PEM-fil er en sikkerhedscertifikatfil, der bruges til at etablere en sikker kommunikationskanal mellem en webserver og en browser. Det er Base64-kodet og kan indeholde en privat nøgle, servercertifikat og/eller en kombination af andre certifikater. PEM-filer ligner .der-certifikatfiler med hensyn til brug, men gemmes som Base64-kodet tekst i stedet for binære data. Andre lignende certifikatfilformater omfatter [.cer](/web/cer/)- og [.crt](/web/crt/)-filer.

Programmer, der kan **åbne PEM-filer**, inkluderer teksteditorer som Microsoft Notepad og Apple TextEdit.

## PEM filformat

PEM er et containerfilformat, der definerer strukturen og kodningstypen for den fil, der bruges til at gemme dataene. PEM-filer gemmes på disken som Base64-kodet filformat, der ikke kan læses af mennesker. Standarden definerer, at en PEM-fil starter med:

```
-----BEGIN <type>-----
```
og slutter med:
```
-----END <type>-----
```

Alt andet indhold i disse er base64-kodet (store og små bogstaver, cifre, + og /). En enkelt PEM-fil kan bestå af flere blokke, som kan bruges af andre programmer. Hvis en PEM-fil indeholder flere certifikater, adskilles hvert certifikat af individuelle blokke som følger:

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

### Eksempel på PEM-fil

En PEM-fil med CERTIFICATE-blok ser normalt ud som følger:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

En PEM-fil med RSA starter som følger.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referencer ##

* [Public-key_cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)

* [Hvordan opretter man P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)


