{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл PEM – формат файлу сертифіката пошти з розширеною конфіденційністю",
  "description":"Дізнайтеся про формат файлу PEM та API, які можуть створювати та відкривати файли PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Що таке файл PEM?

Файл PEM – це файл сертифіката безпеки, який використовується для встановлення безпечного каналу зв’язку між веб-сервером і браузером. Він закодований за допомогою Base64 і може містити закритий ключ, сертифікат сервера та/або комбінацію інших сертифікатів. Файли PEM подібні до файлів сертифікатів .der щодо використання, але зберігаються як текст у кодуванні Base64, а не як двійкові дані. Інші подібні формати файлів сертифікатів включають файли [.cer](/uk/web/cer/) і [.crt](/uk/web/crt/).

Програми, які можуть **відкривати файли PEM**, включають текстові редактори, такі як Microsoft Notepad і Apple TextEdit.

## Формат файлу PEM

PEM — це формат файлу-контейнера, який визначає структуру та тип кодування файлу, що використовується для зберігання даних. Файли PEM зберігаються на диску у форматі файлу, закодованому за допомогою Base64, який не читається людиною. Стандарт визначає, що файл PEM починається з:

```
-----BEGIN <type>-----
```
і закінчується на:
```
-----END <type>-----
```

Весь інший вміст у них кодується base64 (великі та малі літери, цифри, + та /). Один файл PEM може складатися з кількох блоків, які можуть використовуватися іншими програмами. Якщо файл PEM містить кілька сертифікатів, кожен сертифікат відокремлюється окремими блоками наступним чином:

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

### Приклад файлу PEM

Файл PEM із блоком CERTIFICATE зазвичай виглядає так:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Файл PEM із RSA починається так.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Посилання ##

* [Криптографія відкритого ключа](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Як створити файл P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

