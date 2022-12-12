{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу KEY та API, які можуть створювати та відкривати файли KEY.",
  "title" :"Формат файлу KEY - файл закритого ключа електронної пошти з підвищеною конфіденційністю",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Що таке файл KEY?

Файл KEY – це приватна частина механізму безпеки, яка зберігається на диску у форматі Privacy-Enhanced Mal (PEM). Він використовується для розшифровки інформації, якою обмінюються веб-браузер і веб-сервер, який обслуговує запити перегляду. Файл KEY містить закодовані рядки, які марні для людського ока, але є суттю обміну інформацією для шифрування/дешифрування як частини сертифіката SSL на веб-серверах. Файли KEY автоматично генеруються та встановлюються на стороні клієнта.

Ви можете відкривати файли **KEY** за допомогою будь-якого текстового редактора, наприклад Microsoft Notepad (Windows), Apple TextEdit (Mac) або GitHub Atom (кроссплатформенний). Файли KEY схожі на формати файлів [CRT](/uk/web/crt/) і [CER](/uk/web/cer/).

## KEY Формат файлу - Додаткова інформація

Файли KEY зберігаються на диску як звичайні текстові файли, але є закодованими рядками, які людині незручно читати. Практично користувачі не розуміють рядків, коли їх відкривають у текстовому редакторі. Сертифікат закритого ключа є конфіденційним, і його не можна нікому повідомляти. Повний процес забезпечення безпеки обміну інформацією через Інтернет передбачає:

* **Відкритий ключ** - використовується для шифрування інформації користувача для обміну даними між браузером і веб-серверами
* **Приватний ключ** - використовується для розшифровки інформації, яку отримує веб-сервер

Сертифікати SSL, також відомі як сертифікати X.509, є унікальними для кожного веб-сайту. Файли KEY, використовуючи такий синтаксис:

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

### Приклад файлу KEY

Нижче наведено приклад файлу закритого ключа.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Список літератури

* [Відкриті ключі, приватні ключі та сертифікати](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

