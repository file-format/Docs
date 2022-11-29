{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM File - Privacy Enhanced Mail Certificate File Format",
  "description":"Läs mer om PEM-filformat och API:er som kan skapa och öppna PEM-filer.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Vad är en PEM fil?

En PEM-fil är en säkerhetscertifikatfil som används för att upprätta en säker kommunikationskanal mellan en webbserver och en webbläsare. Den är Base64-kodad och kan innehålla en privat nyckel, servercertifikat och/eller en kombination av andra certifikat. PEM-filer liknar .der-certifikatfiler när det gäller användning men lagras som Base64-kodad text snarare än binär data. Andra liknande certifikatfilformat inkluderar filerna [.cer](/sv/web/cer/) och [.crt](/sv/web/crt/).

Applikationer som kan **öppna PEM-filer** inkluderar textredigerare som Microsoft Notepad och Apple TextEdit.

## PEM filformat

PEM är ett containerfilformat som definierar strukturen och kodningstypen för filen som används för att lagra data. PEM-filer lagras på skiva som Base64-kodat filformat som inte är läsbart för människor. Standarden definierar att en PEM-fil börjar med:

```
-----BEGIN <type>-----
```
och slutar med:
```
-----END <type>-----
```

Allt annat innehåll i dessa är base64-kodat (versaler och gemener, siffror, + och /). En enda PEM-fil kan bestå av flera block som kan användas av andra program. Om en PEM-fil innehåller flera certifikat separeras varje certifikat av individuella block enligt följande:

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

### Exempel på PEM-fil

En PEM-fil med CERTIFICATE-block ser vanligtvis ut så här:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

En PEM-fil med RSA börjar som följande.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referenser ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hur skapar jag P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

