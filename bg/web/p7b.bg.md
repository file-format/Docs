{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B – файл със сертификат PKCS 7",
  "description":"Научете повече за P7C файловия формат и API, които могат да създават и отварят P7C файлове.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е P7B файл?

Файлът P7B е файл със сертификат за сигурност, който съдържа защитен цифров сертификат за удостоверяване на лице или устройство. Подобно на файл със сертификат [.cer](/bg/web/cer/), P7B файл може да бъде инсталиран с помощта на опцията „Инсталиране на сертификат“, като използвате опцията за щракване с десния бутон върху файла. P7B използва различна опция за форматиране от файловия формат CER. Той съдържа един или повече файлове с цифров сертификат X.509, които използват кодиране base64 (ASCII). P7B файловете се получават като [ZIP](/bg/compression/zip/) файл или се получават от сертифициращия орган.

## P7B файлов формат

P7B файловете се съхраняват като обикновени ASCII файлове, които могат да бъдат отворени във всеки текстов редактор. Той съдържа публичния ключ, който е кодиран низ, който е безсмислен от гледна точка на четимост.

### Пример за файлов формат P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Препратки ##

* [Криптография с публичен ключ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как да създадете P7C файл?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

