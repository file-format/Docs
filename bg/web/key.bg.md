{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за KEY файловия формат и API, които могат да създават и отварят KEY файлове.",
  "title" :"KEY файлов формат – частен ключов файл за поща с подобрена поверителност",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Какво е KEY файл?

КЛЮЧОВИЯТ файл е личната част от защитен механизъм, който се записва на диск във файлов формат с подобрена поверителност Mal (PEM). Използва се за дешифриране на информация, обменяна между уеб браузър и уеб сървъра, който обслужва заявките за сърфиране. Файлът KEY съдържа кодирани низове, които са безполезни за човешкото око, но са същността на обмена на информация за криптиране/декриптиране като част от SSL сертификат на уеб сървъри. KEY файловете се генерират автоматично и се инсталират в края на клиента.

Можете да отваряте **KEY** файлове с всеки текстов редактор като Microsoft Notepad (Windows), Apple TextEdit (Mac) или GitHub Atom (между платформи). Файловете KEY са подобни на файловите формати [CRT](/bg/web/crt/) и [CER](/bg/web/cer/).

## KEY файлов формат - повече информация

КЛЮЧОВИТЕ файлове се съхраняват на диск като обикновени текстови файлове, но са кодирани низове, които не са лесни за четене. На практика потребителите нямат разбиране за низовете, когато се отварят в текстов редактор. Сертификатът на частния ключ е поверителен и не трябва да се споделя с никого. Пълният процес на осигуряване на обмен на информация по интернет включва:

* **Публичен ключ** - използва се за криптиране на потребителска информация за обмен на данни между браузъра и уеб сървърите
* **Частен ключ** - използва се за дешифриране на информацията, когато е получена от уеб сървъра

SSL сертификатите, известни още като X.509 сертификати, са уникални за всеки уебсайт. KEY файлове, използващи следния синтаксис:

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

### Пример за КЛЮЧОВ файл

Следва пример за частен ключов файл.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Препратки

* [Публични ключове, частни ключове и сертификати](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

