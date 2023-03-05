{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла KEY и API-интерфейсах, которые могут создавать и открывать файлы KEY.",
  "title" :"Формат файла KEY — файл закрытого ключа электронной почты с повышенной конфиденциальностью",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
"идентификатор":"веб-ключ",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .KEY вариант №

Файл KEY — это закрытая часть механизма безопасности, которая сохраняется на диск в формате файла Privacy-Enhanced Mal (PEM). Он используется для расшифровки информации, которой обмениваются веб-браузер и веб-сервер, обслуживающий запросы просмотра. Файл KEY содержит закодированные строки, которые бесполезны для человеческого глаза, но являются сущностью обмена шифрованием/дешифрованием информации как часть SSL-сертификата на веб-серверах. Файлы KEY генерируются автоматически и устанавливаются на стороне клиента.

Вы можете открывать файлы **KEY** в любом текстовом редакторе, таком как Microsoft Notepad (Windows), Apple TextEdit (Mac) или GitHub Atom (кроссплатформенный). Файлы KEY аналогичны форматам файлов [CRT](/ru/web/crt/) и [CER](/ru/web/cer/).

## Формат файла KEY — дополнительная информация

Файлы KEY хранятся на диске в виде простых текстовых файлов, но представляют собой закодированные строки, которые неудобны для чтения человеком. Практически пользователи не понимают, что такое строки при открытии в текстовом редакторе. Сертификат закрытого ключа является конфиденциальным и никому не должен передаваться. Полный процесс обеспечения безопасности обмена информацией через Интернет включает в себя:

* **Открытый ключ** - используется для шифрования информации пользователя для обмена данными между браузером и веб-серверами.
* **Закрытый ключ** — используется для расшифровки информации по мере ее получения веб-сервером.

Сертификаты SSL, также известные как сертификаты X.509, уникальны для каждого веб-сайта. KEY, используя следующий синтаксис:

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

### Пример файла KEY

Ниже приведен пример файла закрытого ключа.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## использованная литература

* [Открытые ключи, закрытые ключи и сертификаты](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

