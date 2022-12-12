{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a KEY fájlformátumról és az API-król, amelyek KEY fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"KEY File Format – fokozott adatvédelemmel ellátott levelezési privát kulcsfájl",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Mi az a KEY fájl?

A KEY-fájl egy biztonsági mechanizmus privát része, amelyet a rendszer Privacy-Enhanced Mal (PEM) fájlformátumban ment a lemezre. A webböngésző és a böngészési kéréseket kiszolgáló webszerver között kicserélt információk visszafejtésére szolgál. A KEY fájl olyan kódolt karakterláncokat tartalmaz, amelyek emberi szem számára haszontalanok, de a webszervereken az SSL-tanúsítvány részeként az információcsere titkosításának/dekódolásának lényegét képezik. A KEY fájlok automatikusan generálódnak és telepítésre kerülnek a kliens végén.

A **KEY** fájlokat bármilyen szövegszerkesztővel megnyithatja, például a Microsoft Notepad (Windows), az Apple TextEdit (Mac) vagy a GitHub Atom (cross-platform) segítségével. A KEY fájlok hasonlóak a [CRT](/hu/web/crt/) és [CER](/hu/web/cer/) fájlformátumokhoz.

## KEY Fájlformátum – További információ

A KEY fájlok egyszerű szöveges fájlokként kerülnek a lemezre, de olyan kódolt karakterláncok, amelyeket nem emberbarát olvasni. Gyakorlatilag a felhasználók nem értik a karakterláncokat, amikor megnyitják őket egy szövegszerkesztőben. A privát kulcs tanúsítványa bizalmas, és nem osztható meg senkivel. Az interneten keresztüli információcsere biztosításának teljes folyamata magában foglalja a következőket:

* **Nyilvános kulcs** - a felhasználó adatainak titkosítására szolgál a böngésző és a webszerverek közötti adatcseréhez
* **Privát kulcs** – a webszerver által fogadott információk visszafejtésére szolgál

Az SSL-tanúsítványok, más néven X.509-tanúsítványok, minden webhely esetében egyediek. KEY fájlok a következő szintaxissal:

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

### KEY fájl példa

A következő egy példa a privát kulcs fájlra.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Hivatkozások

* [Nyilvános kulcsok, privát kulcsok és tanúsítványok](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

