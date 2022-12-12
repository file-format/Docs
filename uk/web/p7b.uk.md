{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Файл сертифіката PKCS 7",
  "description":"Дізнайтеся про формат файлу P7C та API, які можуть створювати та відкривати файли P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл P7B?

Файл P7B — це файл сертифіката безпеки, який містить безпечний цифровий сертифікат для автентифікації особи або пристрою. Подібно до файлу сертифіката [.cer](/uk/web/cer/), файл P7B можна встановити за допомогою параметра «Установити сертифікат», клацнувши правою кнопкою миші на файлі. P7B використовує інший варіант форматування, ніж формат файлу CER. Він містить один або кілька файлів цифрових сертифікатів X.509, які використовують кодування base64 (ASCII). Файли P7B надходять як файл [ZIP](/uk/compression/zip/) або отримуються від центру сертифікації.

## Формат файлу P7B

Файли P7B зберігаються як звичайні файли ASCII, які можна відкрити в будь-якому текстовому редакторі. Він містить відкритий ключ, який є закодованим рядком, який не має сенсу з точки зору читабельності.

### Приклад формату файлу P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Посилання ##

* [Криптографія відкритого ключа](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Як створити файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

