{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om KEY-filformat och API:er som kan skapa och öppna KEY-filer.",
  "title" :"KEY File Format - Privacy-Enhanced Mail Private Key File",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Vad är en KEY fil?

En KEY-fil är den privata delen av en säkerhetsmekanism som sparas på skiva i PEM-filformatet (Privacy-Enhanced Mal). Den används för att dekryptera information som utbyts mellan en webbläsare och webbservern som betjänar webbläsarförfrågningarna. En KEY-fil innehåller kodade strängar som är oanvändbara för det mänskliga ögat men som är kärnan i kryptering/dekryptering av informationsutbyte som en del av SSL-certifikatet på webbservrar. KEY-filer genereras automatiskt och installeras i klientänden.

Du kan öppna **KEY**-filer med vilken textredigerare som helst som Microsoft Notepad (Windows), Apple TextEdit (Mac) eller GitHub Atom (plattformsoberoende). KEY-filer liknar filformaten [CRT](/sv/web/crt/) och [CER](/sv/web/cer/).

## KEY File Format - Mer information

KEY-filer lagras på skiva som vanliga textfiler men är kodade strängar som inte är människovänliga att läsa. Praktiskt taget har användare ingen förståelse för strängarna när de öppnas i en textredigerare. Det privata nyckelcertifikatet är konfidentiellt och bör inte delas med någon. Den fullständiga processen för att säkra informationsutbytet över internet innefattar en:

* **Public Key** - används för att kryptera användarens information för utbyte av data mellan webbläsaren och webbservrarna
* **Privat nyckel** - används för att dekryptera informationen när den tas emot av webbservern

SSL-certifikaten, även kända som X.509-certifikat, är unika för varje webbplats. KEY-filer med följande syntax:

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

### KEY Fil Exempel

Följande är ett exempel på en privat nyckelfil.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenser

* [Offentliga nycklar, privata nycklar och certifikat](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

