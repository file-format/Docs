
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS файл – архив на набор от APK",
  "description":"Научете какво е APKS файл?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Какво е APKS файл?

Файл с разширение .apks е архивен файл, който е колекция от **APK** файлове на Android пакет. Всеки отделен APK файл в APKS файла се генерира, като се отчитат различни аспекти на устройствата. Те включват архитектура, език, плътност на екрана и други характеристики на устройството. APKS файловете се генерират от **bundletool**. Използва се за изграждане на Android App Bundle и конвертиране на пакета приложения в различни APK файлове за внедряване на устройства.

## APKS файлов формат - повече информация

APKS файловете се записват като компресирани файлове с помощта на файлов формат [ZIP](/bg/компресия/zip/).

## Как да генерирам APKS файл?

Когато Android App Bundle (AAB) е готов, поведението му в Google Play Store може да бъде тествано за внедряване на устройство. APKS файловете могат да бъдат генерирани за тази цел от AAB файлове и инсталирани на тестови устройства с помощта на [bundletool] на Google за Android (https://developer.android.com/tools/bundletool). Той предоставя инструменти за команден ред за създаване на APKS архивен файл от APK чрез следната команда.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

За да внедрите APK файловете на устройство, APKS файлът може да бъде подписан с информацията за подписване на устройството, както следва.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Препратки

* [bundletool - команден ред](https://developer.android.com/tools/bundletool)

