{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - soubor certifikátu PKCS 7",
  "description":"Další informace o formátu souborů P7C a rozhraních API, která mohou vytvářet a otevírat soubory P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor P7C?

Soubor P7C, stejně jako jiné soubory bezpečnostních certifikátů, je digitální certifikát, který se používá k ověření identity v síti. Aplikace používající certifikáty ověřují identitu pomocí veřejného klíče obsaženého v těchto souborech certifikátů. Kryptografie s veřejným klíčem nebo asymetrická kryptografie používá pár klíčů, z nichž jeden je veřejný klíč a druhý je známý jako soukromý klíč. Soukromý klíč je zabezpečen pro efektivní zabezpečení, zatímco veřejný klíč lze sdílet s ostatními. Mezi další běžné formáty souborů certifikátů patří [CRT](/cs/web/crt/), DER a PEM.

## Formát souboru P7C – Další informace

Soubory P7C se ukládají na disk jako binární soubory a obsahují informace o veřejném klíči generované pomocí kryptografických algoritmů založených na matematických problémech. Ty lze otevřít v libovolném textovém editoru, ale jejich obsah není v podobě čitelné pro člověka. Některé z aplikací, které mohou otevřít soubory P7C, zahrnují Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager a Microsoft Windows Contacts.

### Příklad formátu souboru P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Reference ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak vytvořit soubor P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

