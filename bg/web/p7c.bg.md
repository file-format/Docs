{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C – файл със сертификат PKCS 7",
  "description":"Научете повече за P7C файловия формат и API, които могат да създават и отварят P7C файлове.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е P7C файл?

P7C файл, подобно на други файлове със сертификати за сигурност, е цифров сертификат, който се използва за удостоверяване на самоличността в мрежата. Приложенията, използващи сертификати, удостоверяват самоличността с помощта на публичния ключ, включен в тези файлове със сертификати. Криптографията с публичен ключ или асиметричната криптография използва двойка ключове, единият от които е публичен ключ, а другият е известен като частен ключ. Частният ключ се пази сигурно за ефективна сигурност, докато публичният ключ може да се споделя с други. Други често срещани файлови формати на сертификати включват [CRT](/bg/web/crt/), DER и PEM.

## P7C файлов формат - повече информация

P7C файловете се записват на диск като двоични файлове и включват информацията за публичния ключ, генерирана с помощта на криптографски алгоритми, базирани на математически проблеми. Те могат да бъдат отворени във всеки текстов редактор, но съдържанието им не е в четима от хора форма. Някои от приложенията, които могат да отварят P7C файлове, включват Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager и Microsoft Windows Contacts.

### Пример за файлов формат P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Препратки ##

* [Криптография с публичен ключ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как да създадете P7C файл?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

