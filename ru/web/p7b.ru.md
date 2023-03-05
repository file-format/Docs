{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B — файл сертификата PKCS 7",
  "description":"Узнайте о формате файла P7C и API, которые могут создавать и открывать файлы P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7B вариант №

Файл P7B — это файл сертификата безопасности, который содержит безопасный цифровой сертификат для аутентификации человека или устройства. Подобно файлу сертификата [.cer](/ru/web/cer/), файл P7B можно установить с помощью параметра «Установить сертификат», щелкнув файл правой кнопкой мыши. P7B использует другой вариант форматирования, чем формат файла CER. Он содержит один или несколько файлов цифровых сертификатов X.509, в которых используется кодировка base64 (ASCII). Файлы P7B принимаются в виде файла [ZIP](/ru/compression/zip/) или получаются из центра сертификации.

## Формат файла P7B

Файлы P7B хранятся в виде простых файлов ASCII, которые можно открыть в любом текстовом редакторе. Он содержит открытый ключ, представляющий собой закодированную строку, которая не имеет смысла с точки зрения удобочитаемости.

### Пример формата файла P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Использованная литература ##

* [Криптография с открытым ключом](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как создать файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

