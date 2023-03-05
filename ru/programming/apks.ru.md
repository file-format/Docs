
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл APK - Архив набора APK",
  "description":"Узнать, что такое файл APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## .APKS вариант №

Файл с расширением .apks представляет собой архивный файл, представляющий собой набор файлов **APK** пакета Android. Каждый отдельный файл APK в файле APKS создается с учетом различных аспектов устройств. К ним относятся архитектура, язык, плотность экрана и другие функции устройства. Файлы APKS генерируются **bundletool**. Он используется для создания Android App Bundle и преобразования пакета приложений в разные APK для развертывания на устройствах.

## Формат файла APKS — дополнительная информация

Файлы APKS сохраняются в виде сжатых файлов в формате [ZIP](/ru/compression/zip/).

## Как создать файл APKS?

Когда Android App Bundle (AAB) готов, его поведение в магазине Google Play можно протестировать для развертывания на устройстве. Для этой цели файлы APKS могут быть сгенерированы из файлов AAB и установлены на тестовых устройствах с помощью Android [bundletool] от Google (https://developer.android.com/studio/command-line/bundletool). Он предоставляет инструменты командной строки для создания файла архива APKS из APK с помощью следующей команды.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Чтобы развернуть APK на устройстве, файл APKS можно подписать информацией о подписи устройства следующим образом.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## использованная литература

* [bundletool — командная строка](https://developer.android.com/studio/command-line/bundletool)

