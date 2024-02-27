{
  "date": "2019-10-11",
  "keywords": [
"crt",
"crt-fil",
"crt filformat",
"crt filtype",
"fil",
"type",
"hvad er en crt-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRT - Sikkerhedscertifikatfilformat",
  "description": "Lær om CRT-filformat og API'er, der kan oprette og åbne CRT-filer.",
  "linktitle": "CRT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en CRT fil?

En fil med filtypenavnet .crt er en sikkerhedscertifikatfil, der bruges af sikre websteder til at etablere sikre forbindelser fra webserveren til en browser. Sikre hjemmesider gør det muligt at sikre dataoverførsler, logins, betalingskorttransaktioner og give beskyttet browsing til siden. Hvis du åbner en sikker hjemmeside, ser du et lås-ikon i adresselinjen. Hvis du klikker på det, kan du se detaljerne for det installerede certifikat. Internationale virksomheder som Verisign og Thawte distribuerer disse SSL-certifikater.

## CRT filformat

CRT-filer er i ASCII-format og kan åbnes i enhver teksteditor for at se indholdet af certifikatfilen. Det følger X.509-certificeringsstandarden, der definerer certifikatets struktur. Den definerer de datafelter, der skal inkluderes i SSL-certifikatet. CRT tilhører PEM-formatet for certifikater, der er Base64 ASCII-kodede filer.

### PEM-filstruktur

En PEM-fil kan have flere certifikater. I et sådant tilfælde følger hvert certifikat i PEM-filen følgende struktur.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Eksempel på CRT-filformat

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencer ##

* [Public Keys, Private Keys, and Certificates](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

