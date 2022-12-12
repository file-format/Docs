{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "crt файл", "crt файл формат", "crt файл тип", "файл", "тип", "какво е crt файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Файлов формат на сертификат за сигурност",
  "description":"Научете за CRT файловия формат и API, които могат да създават и отварят CRT файлове.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е CRT файл?

Файл с разширение .crt е файл със сертификат за сигурност, който се използва от защитени уебсайтове за установяване на защитени връзки от уеб сървър към браузър. Защитените уебсайтове позволяват да се защити трансфер на данни, влизания, транзакции с платежни карти и осигуряват защитено сърфиране в сайта. Ако отворите защитен уебсайт, ще видите икона „заключване“ в адресната лента. Ако щракнете върху него, можете да видите подробностите за инсталирания сертификат. Международни компании като Verisign и Thawte разпространяват тези SSL сертификати.

## CRT файлов формат

CRT файловете са във формат ASCII и могат да бъдат отворени във всеки текстов редактор, за да видите съдържанието на файла със сертификата. Той следва стандарта за сертифициране X.509, който определя структурата на сертификата. Той определя полетата с данни, които трябва да бъдат включени в SSL сертификата. CRT принадлежи към PEM формата на сертификати, които са Base64 ASCII кодирани файлове.

### PEM файлова структура

Един PEM файл може да има множество сертификати. В такъв случай всеки сертификат в PEM файла следва следната структура.

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

### Пример за CRT файлов формат

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Препратки ##

* [Публични ключове, частни ключове и сертификати](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

