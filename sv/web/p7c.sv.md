{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 certifikatfil",
  "description":"Läs mer om P7C-filformat och API:er som kan skapa och öppna P7C-filer.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en P7C fil?

En P7C-fil är, liksom andra säkerhetscertifikatfiler, ett digitalt certifikat som används för att autentisera identitet över nätverket. Applikationer som använder certifikat autentiserar identitet med den publika nyckeln som ingår i dessa certifikatfiler. Public-key kryptografi, eller asymmetrisk kryptografi, använder par nycklar varav en är den offentliga nyckeln och den andra är känd som privat nyckel. Den privata nyckeln hålls säker för effektiv säkerhet, medan den offentliga nyckeln kan delas med andra. Andra vanliga certifikatfilformat inkluderar [CRT](/sv/web/crt/), DER och PEM.

## P7C-filformat - Mer information

P7C-filer sparas på skiva som binära filer och inkluderar den publika nyckelinformationen som genereras med hjälp av kryptografiska algoritmer baserade på matematiska problem. Dessa kan öppnas i vilken textredigerare som helst men deras innehåll är inte i läsbar form. Några av de program som kan öppna P7C-filer inkluderar Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager och Microsoft Windows Contacts.

### Exempel på P7C-filformat

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenser ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hur skapar jag P7C-fil?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

