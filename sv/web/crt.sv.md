{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "crt-fil", "crt-filformat", "crt-filtyp", "fil", "typ", "vad är en crt-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Filformat för säkerhetscertifikat",
  "description":"Läs mer om CRT-filformat och API:er som kan skapa och öppna CRT-filer.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en CRT fil?

En fil med tillägget .crt är en säkerhetscertifikatfil som används av säkra webbplatser för att upprätta säkra anslutningar från webbservern till en webbläsare. Säkra webbplatser gör det möjligt att säkra dataöverföringar, inloggningar, betalkortstransaktioner och tillhandahålla skyddad surfning till webbplatsen. Om du öppnar en säker webbplats ser du en "lås"-ikon i adressfältet. Om du klickar på den kan du se detaljerna för det installerade certifikatet. Internationella företag som Verisign och Thawte distribuerar dessa SSL-certifikat.

## CRT-filformat

CRT-filer är i ASCII-format och kan öppnas i valfri textredigerare för att se innehållet i certifikatfilen. Den följer certifieringsstandarden X.509 som definierar certifikatets struktur. Den definierar de datafält som ska inkluderas i SSL-certifikatet. CRT tillhör PEM-formatet för certifikat som är Base64 ASCII-kodade filer.

### PEM-filstruktur

En PEM-fil kan ha flera certifikat. I ett sådant fall följer varje certifikat i PEM-filen följande struktur.

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

### Exempel på CRT-filformat

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenser ##

* [Offentliga nycklar, privata nycklar och certifikat](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

