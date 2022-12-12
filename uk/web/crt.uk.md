{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "файл crt", "формат файлу crt", "тип файлу crt", "файл", "тип", "що таке файл crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - формат файлу сертифіката безпеки",
  "description":"Дізнайтеся про формат файлу CRT та API, які можуть створювати та відкривати файли CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл CRT?

Файл із розширенням .crt — це файл сертифіката безпеки, який використовується безпечними веб-сайтами для встановлення безпечних з’єднань від веб-сервера до браузера. Захищені веб-сайти дають змогу безпечно передавати дані, логіни, транзакції платіжними картками та забезпечують захищений перегляд сайту. Якщо ви відкриваєте захищений веб-сайт, в адресному рядку ви побачите значок замка. Якщо натиснути на нього, можна переглянути деталі встановленого сертифіката. Міжнародні компанії, такі як Verisign і Thawte, поширюють ці сертифікати SSL.

## Формат файлу CRT

Файли CRT мають формат ASCII і їх можна відкрити в будь-якому текстовому редакторі, щоб переглянути вміст файлу сертифіката. Він відповідає стандарту сертифікації X.509, який визначає структуру сертифіката. Він визначає поля даних, які повинні бути включені в сертифікат SSL. CRT належить до формату PEM сертифікатів, які є файлами в кодуванні Base64 ASCII.

### Структура файлу PEM

Файл PEM може мати кілька сертифікатів. У такому випадку кожен сертифікат у файлі PEM має таку структуру.

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

### Приклад формату файлу CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Посилання ##

* [Відкриті ключі, приватні ключі та сертифікати](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

