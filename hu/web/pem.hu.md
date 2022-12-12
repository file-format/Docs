{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM-fájl – fokozott adatvédelmi levéltanúsítvány-fájlformátum",
  "description":"További információ a PEM-fájlformátumról és az API-król, amelyek PEM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Mi az a PEM fájl?

A PEM-fájl egy biztonsági tanúsítványfájl, amely biztonságos kommunikációs csatorna létrehozására szolgál a webszerver és a böngésző között. Base64 kódolású, és tartalmazhat privát kulcsot, szervertanúsítványt és/vagy egyéb tanúsítványok kombinációját. A PEM-fájlok használatukat tekintve hasonlóak a .der-tanúsítványfájlokhoz, de bináris adatok helyett Base64-kódolású szövegként tárolódnak. További hasonló tanúsítványfájlformátumok közé tartoznak a [.cer](/hu/web/cer/) és a [.crt](/hu/web/crt/) fájlok.

A **PEM-fájlok megnyitására** képes alkalmazások közé tartoznak a szövegszerkesztők, például a Microsoft Notepad és az Apple TextEdit.

## PEM fájl formátum

A PEM egy konténerfájl formátum, amely meghatározza az adatok tárolására használt fájl szerkezetét és kódolási típusát. A PEM fájlok Base64 kódolású, ember által nem olvasható fájlformátumban tárolódnak a lemezen. A szabvány meghatározza, hogy a PEM fájl a következővel kezdődik:

```
-----BEGIN <type>-----
```
és így végződik:
```
-----END <type>-----
```

Az ezeken belüli összes többi tartalom base64 kódolású (nagy- és kisbetűk, számjegyek, + és /). Egyetlen PEM-fájl több blokkot is tartalmazhat, amelyeket más programok is használhatnak. Ha egy PEM-fájl több tanúsítványt is tartalmaz, minden tanúsítványt külön blokkok választanak el az alábbiak szerint:

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

### PEM fájl példa

A CERTIFICATE blokkal rendelkező PEM-fájl általában így néz ki:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Az RSA-val rendelkező PEM-fájl a következőképpen kezdődik.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Hivatkozások ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hogyan hozhatunk létre P7C-fájlt?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

