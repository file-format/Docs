{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 tanúsítványfájl",
  "description":"További információ a P7C fájlformátumról és az API-król, amelyek P7C fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a P7C fájl?

A P7C-fájl más biztonsági tanúsítványfájlokhoz hasonlóan egy digitális tanúsítvány, amelyet a hálózaton keresztüli azonosításra használnak. A tanúsítványokat használó alkalmazások a tanúsítványfájlokban található nyilvános kulccsal hitelesítik az azonosságot. A nyilvános kulcsú kriptográfia vagy az aszimmetrikus kriptográfia kulcspárt használ, amelyek közül az egyik a nyilvános kulcs, a másik pedig a privát kulcs. A privát kulcsot biztonságosan tartják a hatékony biztonság érdekében, míg a nyilvános kulcsot meg lehet osztani másokkal. Egyéb gyakori tanúsítványfájlformátumok: [CRT](/hu/web/crt/), DER és PEM.

## P7C fájlformátum - További információ

A P7C fájlok bináris fájlként kerülnek a lemezre, és tartalmazzák a matematikai problémákon alapuló kriptográfiai algoritmusokkal előállított nyilvános kulcsú információkat. Ezek bármelyik szövegszerkesztőben megnyithatók, de tartalmuk nem ember által olvasható formában. A P7C fájlokat megnyitni képes alkalmazások közé tartozik az Apple Keychain Access, az Adobe Acrobat Reader DC, a Microsoft Certificate Manager és a Microsoft Windows Contacts.

### P7C fájlformátum példa

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Hivatkozások ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Hogyan hozhatunk létre P7C-fájlt?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

