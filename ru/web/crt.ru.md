{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "crt файл", "формат файла crt", "тип файла crt", "файл", "тип", "что такое файл crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT — формат файла сертификата безопасности",
  "description":"Узнайте о формате файла CRT и API-интерфейсах, которые могут создавать и открывать файлы CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .CRT вариант №

Файл с расширением .crt — это файл сертификата безопасности, который используется безопасными веб-сайтами для установления безопасных соединений с веб-сервера на браузер. Защищенные веб-сайты позволяют защитить передачу данных, вход в систему, операции с платежными картами и обеспечить защищенный просмотр сайта. Если вы откроете безопасный веб-сайт, вы увидите значок «замок» в адресной строке. Если вы нажмете на нее, вы сможете просмотреть сведения об установленном сертификате. Такие SSL-сертификаты распространяют такие международные компании, как Verisign и Thawte.

## Формат файла CRT

Файлы CRT имеют формат ASCII и могут быть открыты в любом текстовом редакторе для просмотра содержимого файла сертификата. Он соответствует стандарту сертификации X.509, который определяет структуру сертификата. Он определяет поля данных, которые должны быть включены в сертификат SSL. CRT относится к формату сертификатов PEM, которые представляют собой файлы в кодировке Base64 ASCII.

### Структура файла PEM

Файл PEM может иметь несколько сертификатов. В таком случае каждый сертификат в файле PEM имеет следующую структуру.

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

### Пример формата файла CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Использованная литература ##

* [Открытые ключи, закрытые ключи и сертификаты] (https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

