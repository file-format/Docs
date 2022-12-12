{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - soubor certifikátu PKCS 7",
  "description":"Další informace o formátu souborů P7C a rozhraních API, která mohou vytvářet a otevírat soubory P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor P7B?

Soubor P7B je soubor bezpečnostního certifikátu, který obsahuje bezpečný digitální certifikát pro ověření osoby nebo zařízení. Podobně jako soubor certifikátu [.cer](/cs/web/cer/) lze soubor P7B nainstalovat pomocí možnosti "Instalovat certifikát" kliknutím pravým tlačítkem na soubor. P7B používá jinou možnost formátování než formát souboru CER. Obsahuje jeden nebo více souborů digitálních certifikátů X.509, které používají kódování base64 (ASCII). Soubory P7B jsou přijímány jako soubor [ZIP](/cs/compression/zip/) nebo přijaté od certifikační autority.

## Formát souboru P7B

Soubory P7B jsou uloženy jako prosté soubory ASCII, které lze otevřít v libovolném textovém editoru. Obsahuje veřejný klíč, což je zakódovaný řetězec, který je z hlediska čitelnosti bezvýznamný.

### Příklad formátu souboru P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Reference ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak vytvořit soubor P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

