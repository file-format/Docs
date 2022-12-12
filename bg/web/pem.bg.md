{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM файл – Файлов формат на пощенски сертификат с подобрена поверителност",
  "description":"Научете за PEM файловия формат и API, които могат да създават и отварят PEM файлове.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Какво е PEM файл?

PEM файлът е файл със сертификат за сигурност, който се използва за установяване на защитен канал за комуникация между уеб сървър и браузър. Той е кодиран с Base64 и може да съдържа частен ключ, сървърен сертификат и/или комбинация от други сертификати. PEM файловете са подобни на .der файловете със сертификати по отношение на използването, но се съхраняват като Base64-кодиран текст, а не като двоични данни. Други подобни файлови формати на сертификати включват [.cer](/bg/web/cer/) и [.crt](/bg/web/crt/) файлове.

Приложенията, които могат да **отварят PEM файлове** включват текстови редактори като Microsoft Notepad и Apple TextEdit.

## PEM файлов формат

PEM е контейнерен файлов формат, който определя структурата и типа на кодиране на файла, използван за съхраняване на данните. PEM файловете се съхраняват на диск като Base64-кодиран файлов формат, който не е четим от хора. Стандартът определя, че PEM файлът започва с:

```
-----BEGIN <type>-----
```
и завършва с:
```
-----END <type>-----
```

Цялото друго съдържание в тях е кодирано base64 (главни и малки букви, цифри, + и /). Един PEM файл може да се състои от множество блокове, които могат да се използват от други програми. Ако PEM файл съдържа множество сертификати, всеки сертификат е разделен от отделни блокове, както следва:

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

### Пример за PEM файл

PEM файл с блок CERTIFICATE обикновено изглежда по следния начин:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

PEM файл с RSA започва както следва.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Препратки ##

* [Криптография с публичен ключ](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Как да създадете P7C файл?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

