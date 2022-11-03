{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл PEM — формат файла почтового сертификата с повышенной конфиденциальностью",
  "description":"Узнайте о формате файла PEM и API-интерфейсах, которые могут создавать и открывать файлы PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## .PEM вариант №

Файл PEM — это файл сертификата безопасности, который используется для установления безопасного канала связи между веб-сервером и браузером. Он имеет кодировку Base64 и может содержать закрытый ключ, сертификат сервера и/или комбинацию других сертификатов. Файлы PEM аналогичны файлам сертификатов .der с точки зрения использования, но хранятся в виде текста в кодировке Base64, а не двоичных данных. Другие подобные форматы файлов сертификатов включают файлы [.cer](/ru/web/cer/) и [.crt](/ru/web/crt/).

Приложения, которые могут **открывать файлы PEM**, включают текстовые редакторы, такие как Microsoft Notepad и Apple TextEdit.

## Формат файла PEM

PEM — это формат файла-контейнера, который определяет структуру и тип кодировки файла, используемого для хранения данных. Файлы PEM хранятся на диске в формате файлов с кодировкой Base64, который не читается человеком. Стандарт определяет, что файл PEM начинается с:

```
-----BEGIN <type>-----
```
и заканчивается:
```
-----END <type>-----
```

Все остальное содержимое внутри них закодировано в base64 (прописные и строчные буквы, цифры, + и /). Один файл PEM может состоять из нескольких блоков, которые могут использоваться другими программами. Если файл PEM содержит несколько сертификатов, каждый сертификат разделяется отдельными блоками следующим образом:

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

### Пример файла PEM

Файл PEM с блоком CERTIFICATE обычно выглядит следующим образом:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Файл PEM с RSA начинается следующим образом.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Использованная литература ##

* [Криптография с открытым ключом] (https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как создать файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

