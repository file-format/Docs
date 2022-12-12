{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Файл сертифіката PKCS 7",
  "description":"Дізнайтеся про формат файлу P7C та API, які можуть створювати та відкривати файли P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл P7C?

Файл P7C, як і інші файли сертифікатів безпеки, є цифровим сертифікатом, який використовується для автентифікації особи в мережі. Програми, які використовують сертифікати, перевіряють автентичність за допомогою відкритого ключа, включеного в ці файли сертифікатів. Криптографія з відкритим ключем, або асиметрична криптографія, використовує пару ключів, один з яких є відкритим ключем, а інший відомий як закритий ключ. Приватний ключ надійно зберігається для ефективної безпеки, а відкритим ключем можна поділитися з іншими. Інші поширені формати файлів сертифікатів включають [CRT](/uk/web/crt/), DER і PEM.

## Формат файлу P7C – Додаткова інформація

Файли P7C зберігаються на диску як двійкові файли та містять інформацію про відкритий ключ, згенеровану за допомогою криптографічних алгоритмів на основі математичних задач. Їх можна відкрити в будь-якому текстовому редакторі, але їхній вміст не в зрозумілій людині формі. Деякі програми, які можуть відкривати файли P7C, включають Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager і Microsoft Windows Contacts.

### Приклад формату файлу P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Посилання ##

* [Криптографія відкритого ключа](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Як створити файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

