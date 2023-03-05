{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C — файл сертификата PKCS 7",
  "description":"Узнайте о формате файла P7C и API, которые могут создавать и открывать файлы P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7C вариант №

Файл P7C, как и другие файлы сертификатов безопасности, представляет собой цифровой сертификат, который используется для аутентификации личности в сети. Приложения, использующие сертификаты, аутентифицируют личность с помощью открытого ключа, включенного в эти файлы сертификатов. Криптография с открытым ключом или асимметричная криптография использует пару ключей, один из которых является открытым ключом, а другой известен как закрытый ключ. Закрытый ключ хранится в надежном месте для обеспечения эффективной безопасности, а открытый ключ может быть передан другим пользователям. Другие распространенные форматы файлов сертификатов включают [CRT](/ru/web/crt/), DER и PEM.

## Формат файла P7C — дополнительная информация

Файлы P7C сохраняются на диск в виде двоичных файлов и содержат информацию об открытом ключе, сгенерированную с использованием криптографических алгоритмов, основанных на математических задачах. Их можно открыть в любом текстовом редакторе, но их содержимое не в удобочитаемой форме. Некоторые из приложений, которые могут открывать файлы P7C, включают Apple Keychain Access, Adobe Acrobat Reader DC, диспетчер сертификатов Microsoft и контакты Microsoft Windows.

### Пример формата файла P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Использованная литература ##

* [Криптография с открытым ключом](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как создать файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

