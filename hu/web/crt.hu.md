{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "crt fájl", "crt fájl formátum", "crt fájl típusa", "fájl", "típus", "mi az a crt fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT – biztonsági tanúsítvány fájlformátuma",
  "description":"További információ a CRT-fájlformátumról és az API-król, amelyek CRT-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a CRT fájl?

A .crt kiterjesztésű fájl egy biztonsági tanúsítványfájl, amelyet biztonságos webhelyek használnak a webszerver és a böngésző közötti biztonságos kapcsolat létrehozására. A biztonságos weboldalak lehetővé teszik az adatátvitel, a bejelentkezés, a fizetési kártyás tranzakciók biztonságossá tételét, valamint a biztonságos böngészést az oldalon. Ha biztonságos webhelyet nyit meg, a címsorban egy „zár” ikon látható. Ha rákattint, megtekintheti a telepített tanúsítvány részleteit. Nemzetközi vállalatok, például a Verisign és a Thawte forgalmazzák ezeket az SSL-tanúsítványokat.

## CRT fájl formátum

A CRT fájlok ASCII formátumúak, és bármely szövegszerkesztőben megnyithatók a tanúsítványfájl tartalmának megtekintéséhez. Az X.509 tanúsítási szabványt követi, amely meghatározza a tanúsítvány szerkezetét. Meghatározza azokat az adatmezőket, amelyeket az SSL-tanúsítványnak tartalmaznia kell. A CRT azon tanúsítványok PEM formátumába tartozik, amelyek Base64 ASCII kódolású fájlok.

### PEM fájlstruktúra

Egy PEM-fájl több tanúsítvánnyal is rendelkezhet. Ebben az esetben a PEM-fájlban lévő minden tanúsítvány a következő struktúrát követi.

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

### CRT fájlformátum példa

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referenciák ##

* [Nyilvános kulcsok, privát kulcsok és tanúsítványok](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

